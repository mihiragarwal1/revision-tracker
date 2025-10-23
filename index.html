import React, { useState } from 'react';

export default function JeeRevisionTracker() {
  const subjects = ['Physics', 'Physical Chemistry', 'Inorganic Chemistry', 'Organic Chemistry', 'Math'];
  const [topics, setTopics] = useState({});
  const [newTopic, setNewTopic] = useState('');
  const [selectedSubject, setSelectedSubject] = useState(subjects[0]);
  const [collapsedSubjects, setCollapsedSubjects] = useState({});

  const revisionIntervals = [1, 3, 6, 10, 15, 21, 28, 36, 45]; // gradual increase

  const addTopic = () => {
    if (!newTopic.trim()) return;
    const now = new Date();
    const nextRevisions = revisionIntervals.map(d => {
      const date = new Date(now);
      date.setDate(now.getDate() + d);
      return date;
    });

    setTopics(prev => ({
      ...prev,
      [selectedSubject]: [
        ...(prev[selectedSubject] || []),
        { name: newTopic, revisions: nextRevisions, done: false, learned: false }
      ]
    }));
    setNewTopic('');
  };

  const markDone = (subject, index) => {
    setTopics(prev => {
      const updated = { ...prev };
      updated[subject][index].done = true;
      return updated;
    });
  };

  const markLearned = (subject, index) => {
    setTopics(prev => {
      const updated = { ...prev };
      updated[subject][index].learned = true;
      return updated;
    });
  };

  const deleteTopic = (subject, index) => {
    setTopics(prev => {
      const updated = { ...prev };
      updated[subject].splice(index, 1);
      return updated;
    });
  };

  const toggleCollapse = subject => {
    setCollapsedSubjects(prev => ({ ...prev, [subject]: !prev[subject] }));
  };

  const today = new Date().toDateString();
  const todayRevisions = Object.entries(topics).flatMap(([subject, subjectTopics]) =>
    (subjectTopics || []).filter(t => !t.learned && t.revisions.some(r => r.toDateString() === today)).map(t => ({ subject, name: t.name }))
  );

  return (
    <div className="p-6 text-center bg-gray-50 min-h-screen">
      <h1 className="text-3xl font-bold mb-6 text-blue-700">JEE Revision Tracker</h1>

      <div className="bg-white p-4 rounded-lg shadow-md mb-6">
        <h2 className="text-xl font-semibold mb-3 text-gray-700">Today's Revisions</h2>
        {todayRevisions.length === 0 ? (
          <p className="text-gray-500">No revisions scheduled for today 🎉</p>
        ) : (
          <ul className="space-y-2">
            {todayRevisions.map((rev, i) => (
              <li key={i} className="p-2 border rounded bg-yellow-100">
                <strong>{rev.name}</strong> <span className="text-gray-600">({rev.subject})</span>
              </li>
            ))}
          </ul>
        )}
      </div>

      <div className="flex justify-center gap-2 mb-6">
        <select
          value={selectedSubject}
          onChange={e => setSelectedSubject(e.target.value)}
          className="border p-2 rounded text-gray-700"
        >
          {subjects.map(s => (
            <option key={s} value={s}>{s}</option>
          ))}
        </select>

        <input
          type="text"
          placeholder="Enter topic name"
          value={newTopic}
          onChange={e => setNewTopic(e.target.value)}
          className="border p-2 rounded w-64"
        />
        <button onClick={addTopic} className="bg-blue-500 text-white px-4 py-2 rounded hover:bg-blue-600">Add</button>
      </div>

      <h2 className="text-xl font-semibold mb-3 text-gray-700">All Topics</h2>
      {subjects.map(subject => (
        <div key={subject} className="mb-4 border rounded-lg shadow-sm bg-white">
          <div className="flex justify-between items-center p-3 bg-gray-200 rounded-t-lg cursor-pointer" onClick={() => toggleCollapse(subject)}>
            <h3 className="font-semibold text-lg text-gray-800">{subject}</h3>
            <span className="text-sm text-gray-600">{collapsedSubjects[subject] ? '▼' : '▲'}</span>
          </div>

          {!collapsedSubjects[subject] && (
            <ul className="p-3 space-y-3">
              {(topics[subject] || []).length === 0 ? (
                <p className="text-gray-500 italic">No topics added yet</p>
              ) : (
                topics[subject].map((topic, index) => (
                  <li key={index} className={`p-3 border rounded-lg flex flex-col bg-gray-50 hover:bg-gray-100 transition-all`}>                    
                    <div className="flex justify-between items-center">
                      <span className={`font-medium text-gray-800 ${topic.learned ? 'opacity-50' : ''}`}>{topic.name}</span>
                      <div className="flex gap-2">
                        {!topic.done && !topic.learned && (
                          <button
                            onClick={() => markDone(subject, index)}
                            className="bg-red-500 text-white px-2 py-1 rounded hover:bg-red-600"
                          >Mark Done</button>
                        )}
                        {!topic.learned && (
                          <button
                            onClick={() => markLearned(subject, index)}
                            className="bg-green-500 text-white px-2 py-1 rounded hover:bg-green-600"
                          >I Know It</button>
                        )}
                        <button
                          onClick={() => deleteTopic(subject, index)}
                          className="bg-gray-400 text-white px-2 py-1 rounded hover:bg-gray-500"
                        >Delete</button>
                      </div>
                    </div>
                    <div className="text-sm text-gray-600 mt-1">
                      Next revisions: {topic.revisions.slice(0, 2).map(d => d.toLocaleDateString()).join(', ')}
                    </div>
                  </li>
                ))
              )}
            </ul>
          )}
        </div>
      ))}
    </div>
  );
}
