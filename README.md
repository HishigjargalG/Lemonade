# Lemonade
import React from "react"; import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button"; import { Input } from "@/components/ui/input"; import { useState } from "react"; import { Star } from "lucide-react";

export default function HomePage() { const [searchTerm, setSearchTerm] = useState(""); const [mangaList, setMangaList] = useState([ { id: 1, title: "Solo Leveling", poster: "/solo-leveling.jpg", rating: 4.8, chapters: ["Chapter 1", "Chapter 2"], }, { id: 2, title: "One Punch Man", poster: "/opm.jpg", rating: 4.6, chapters: ["Chapter 1", "Chapter 2"], }, ]);

const filteredList = mangaList.filter((manga) => manga.title.toLowerCase().includes(searchTerm.toLowerCase()) );

return ( <div className="min-h-screen bg-gray-100 p-4"> <div className="max-w-3xl mx-auto text-center"> <h1 className="text-3xl font-bold mb-4">Манга Орчуулгын Вэб</h1>

