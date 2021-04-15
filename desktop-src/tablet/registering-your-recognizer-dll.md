---
description: A DLL do reconhecedor deve ser registrada para que a plataforma do Tablet PC o use. O reconhecedor deve fazer as seguintes alterações no registro na instalação.
ms.assetid: 1f1d826b-3968-424b-8da8-b69590058ff1
title: Registrando a DLL do reconhecedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51114f11868e6d45dc4d319dab60e5b4f094ddbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506268"
---
# <a name="registering-your-recognizer-dll"></a><span data-ttu-id="08b73-104">Registrando a DLL do reconhecedor</span><span class="sxs-lookup"><span data-stu-id="08b73-104">Registering Your Recognizer DLL</span></span>

<span data-ttu-id="08b73-105">A DLL do reconhecedor deve ser registrada para que a plataforma do Tablet PC o use.</span><span class="sxs-lookup"><span data-stu-id="08b73-105">Your recognizer DLL must be registered for the Tablet PC Platform to use it.</span></span> <span data-ttu-id="08b73-106">O reconhecedor deve fazer as seguintes alterações no registro na instalação.</span><span class="sxs-lookup"><span data-stu-id="08b73-106">The recognizer must make the following changes to the registry at installation.</span></span>

<span data-ttu-id="08b73-107">Adicione uma nova chave para cada um dos CLSIDs do reconhecedor na chave HKEY \_ local \_ /software/Microsoft/TPG/Recognizers/Registry.</span><span class="sxs-lookup"><span data-stu-id="08b73-107">Add a new key for each of the CLSIDs of your recognizer under the HKEY\_LOCAL\_MACHINE/SOFTWARE/Microsoft/TPG/Recognizers/ registry key.</span></span> <span data-ttu-id="08b73-108">Adicione um CLSID por idioma.</span><span class="sxs-lookup"><span data-stu-id="08b73-108">Add one CLSID per language.</span></span> <span data-ttu-id="08b73-109">A tabela a seguir descreve os valores que devem ser adicionados abaixo de cada uma das chaves que contêm seus CLSIDs.</span><span class="sxs-lookup"><span data-stu-id="08b73-109">The following table describes the values that should be added underneath each of the keys containing your CLSIDs.</span></span>

> [!Note]  
> <span data-ttu-id="08b73-110">Os nomes desses valores diferenciam maiúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="08b73-110">The names of these values are case sensitive.</span></span>

 



| <span data-ttu-id="08b73-111">Nome do valor</span><span class="sxs-lookup"><span data-stu-id="08b73-111">Value name</span></span>                             | <span data-ttu-id="08b73-112">Tipo de valor</span><span class="sxs-lookup"><span data-stu-id="08b73-112">Value type</span></span>             | <span data-ttu-id="08b73-113">Descrição do valor</span><span class="sxs-lookup"><span data-stu-id="08b73-113">Value description</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="08b73-114">Sinalizadores de capacidade do reconhecedor</span><span class="sxs-lookup"><span data-stu-id="08b73-114">Recognizer Capability Flags</span></span><br/> | <span data-ttu-id="08b73-115">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="08b73-115">REG\_DWORD</span></span><br/>  | <span data-ttu-id="08b73-116">DWORD usado para determinar os recursos do reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="08b73-116">DWORD used to determine the capabilities of the recognizer.</span></span><br/>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="08b73-117">DLL do reconhecedor</span><span class="sxs-lookup"><span data-stu-id="08b73-117">Recognizer DLL</span></span><br/>              | <span data-ttu-id="08b73-118">REG \_ sz</span><span class="sxs-lookup"><span data-stu-id="08b73-118">REG\_SZ</span></span><br/>     | <span data-ttu-id="08b73-119">Caminho completo para a DLL do reconhecedor instalado.</span><span class="sxs-lookup"><span data-stu-id="08b73-119">Full path to the installed recognizer DLL.</span></span><br/>                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="08b73-120">Idiomas reconhecidos</span><span class="sxs-lookup"><span data-stu-id="08b73-120">Recognized Languages</span></span><br/>        | <span data-ttu-id="08b73-121">\_binário reg</span><span class="sxs-lookup"><span data-stu-id="08b73-121">REG\_BINARY</span></span><br/> | <span data-ttu-id="08b73-122">Matriz binária que descreve a linguagem ou os idiomas com os quais um reconhecedor foi projetado para trabalhar.</span><span class="sxs-lookup"><span data-stu-id="08b73-122">Binary array describing the language or languages that a recognizer is designed to work with.</span></span><br/> <span data-ttu-id="08b73-123">Em recognizes. h, as \_ linguagens máximas definem especifica o número máximo de idiomas com suporte de um reconhecedor, e cada idioma usa uma palavra para armazenar no item "idiomas reconhecidos".</span><span class="sxs-lookup"><span data-stu-id="08b73-123">In rectypes.h, the MAX\_LANGUAGES define specifies the maximum number of languages supported by a recognizer, and each language takes a WORD to store in the "Recognized Languages" item.</span></span> <span data-ttu-id="08b73-124">O tamanho da entrada de \_ registro binário reg deve ser o \_ máximo \* de idiomas sizeof (Word).</span><span class="sxs-lookup"><span data-stu-id="08b73-124">The size of the REG\_BINARY registry entry should be MAX\_LANGUAGES \* sizeof(WORD).</span></span><br/> |



 

 

 




