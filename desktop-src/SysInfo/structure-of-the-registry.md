---
description: O Registro é um banco de dados hierárquico que contém dados que são essenciais para a operação do Windows e os aplicativos e serviços executados no Windows.
ms.assetid: 4ed60563-73d8-4134-8cb2-8388734fb18d
title: Estrutura do Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bf104806b5e4e10b4be7387018e714a0db8bf37
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386665"
---
# <a name="structure-of-the-registry"></a><span data-ttu-id="9d213-103">Estrutura do Registro</span><span class="sxs-lookup"><span data-stu-id="9d213-103">Structure of the Registry</span></span>

<span data-ttu-id="9d213-104">O Registro é um banco de dados hierárquico que contém dados que são essenciais para a operação do Windows e os aplicativos e serviços executados no Windows.</span><span class="sxs-lookup"><span data-stu-id="9d213-104">The registry is a hierarchical database that contains data that is critical for the operation of Windows and the applications and services that run on Windows.</span></span> <span data-ttu-id="9d213-105">Os dados são estruturados em um formato de árvore.</span><span class="sxs-lookup"><span data-stu-id="9d213-105">The data is structured in a tree format.</span></span> <span data-ttu-id="9d213-106">Cada nó na árvore é chamado de *chave*.</span><span class="sxs-lookup"><span data-stu-id="9d213-106">Each node in the tree is called a *key*.</span></span> <span data-ttu-id="9d213-107">Cada chave pode conter *subkeys e* entradas de dados chamadas *valores*.</span><span class="sxs-lookup"><span data-stu-id="9d213-107">Each key can contain both *subkeys* and data entries called *values*.</span></span> <span data-ttu-id="9d213-108">Às vezes, a presença de uma chave são todos os dados que um aplicativo requer; outras vezes, um aplicativo abre uma chave e usa os valores associados à chave.</span><span class="sxs-lookup"><span data-stu-id="9d213-108">Sometimes, the presence of a key is all the data that an application requires; other times, an application opens a key and uses the values associated with the key.</span></span> <span data-ttu-id="9d213-109">Uma chave pode ter qualquer número de valores e os valores podem estar em qualquer formulário.</span><span class="sxs-lookup"><span data-stu-id="9d213-109">A key can have any number of values, and the values can be in any form.</span></span> <span data-ttu-id="9d213-110">Para obter mais informações, consulte [Tipos de valor do Registro](registry-value-types.md) e Limites de tamanho do elemento do [Registro](registry-element-size-limits.md).</span><span class="sxs-lookup"><span data-stu-id="9d213-110">For more information, see [Registry Value Types](registry-value-types.md) and [Registry Element Size Limits](registry-element-size-limits.md).</span></span>

<span data-ttu-id="9d213-111">Cada chave tem um nome que consiste em um ou mais caracteres imprimíveis.</span><span class="sxs-lookup"><span data-stu-id="9d213-111">Each key has a name consisting of one or more printable characters.</span></span> <span data-ttu-id="9d213-112">Os nomes de chave não são sensíveis a minúsculas.</span><span class="sxs-lookup"><span data-stu-id="9d213-112">Key names are not case sensitive.</span></span> <span data-ttu-id="9d213-113">Os nomes de chave não podem incluir o caractere de faixa invertida ( \\ ), mas qualquer outro caractere imprimível pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="9d213-113">Key names cannot include the backslash character (\\), but any other printable character can be used.</span></span> <span data-ttu-id="9d213-114">Os nomes de valor e os dados podem incluir o caractere de faixa invertida.</span><span class="sxs-lookup"><span data-stu-id="9d213-114">Value names and data can include the backslash character.</span></span>

<span data-ttu-id="9d213-115">O nome de cada sub-chave é exclusivo em relação à chave que está imediatamente acima dela na hierarquia.</span><span class="sxs-lookup"><span data-stu-id="9d213-115">The name of each subkey is unique with respect to the key that is immediately above it in the hierarchy.</span></span> <span data-ttu-id="9d213-116">Os nomes de chave não são localizados em outros idiomas, embora os valores possam ser.</span><span class="sxs-lookup"><span data-stu-id="9d213-116">Key names are not localized into other languages, although values may be.</span></span>

<span data-ttu-id="9d213-117">A ilustração a seguir é um exemplo de estrutura de chave do Registro, conforme exibido pelo Editor do Registro.</span><span class="sxs-lookup"><span data-stu-id="9d213-117">The following illustration is an example registry key structure as displayed by the Registry Editor.</span></span>

![janela do editor do Registro](images/regtree.png)

<span data-ttu-id="9d213-119">Cada uma das árvores sob **Meu Computador** é uma chave.</span><span class="sxs-lookup"><span data-stu-id="9d213-119">Each of the trees under **My Computer** is a key.</span></span> <span data-ttu-id="9d213-120">A **chave HKEY \_ LOCAL \_ MACHINE** tem as seguintes sub-chaves: **HARDWARE,** **SAM,** **SECURITY,** **SOFTWARE** e **SYSTEM.**</span><span class="sxs-lookup"><span data-stu-id="9d213-120">The **HKEY\_LOCAL\_MACHINE** key has the following subkeys: **HARDWARE**, **SAM**, **SECURITY**, **SOFTWARE**, and **SYSTEM**.</span></span> <span data-ttu-id="9d213-121">Cada uma dessas chaves, por sua vez, tem sub-chaves.</span><span class="sxs-lookup"><span data-stu-id="9d213-121">Each of these keys in turn has subkeys.</span></span> <span data-ttu-id="9d213-122">Por exemplo, a **chave de HARDWARE** tem as sub-chaves **DESCRIPTION,** **DEVICEMAP** e **RESOURCEMAP**; a **chave DEVICEMAP** tem várias sub-chaves, incluindo **VIDEO.**</span><span class="sxs-lookup"><span data-stu-id="9d213-122">For example, the **HARDWARE** key has the subkeys **DESCRIPTION**, **DEVICEMAP**, and **RESOURCEMAP**; the **DEVICEMAP** key has several subkeys including **VIDEO**.</span></span>

<span data-ttu-id="9d213-123">Cada valor consiste em um nome de valor e seus dados associados, se algum.</span><span class="sxs-lookup"><span data-stu-id="9d213-123">Each value consists of a value name and its associated data, if any.</span></span> <span data-ttu-id="9d213-124">**MaxObjectNumber** e **VgaCompatible são** valores que contêm dados na sub-chave **VIDEO.**</span><span class="sxs-lookup"><span data-stu-id="9d213-124">**MaxObjectNumber** and **VgaCompatible** are values that contain data under the **VIDEO** subkey.</span></span>

<span data-ttu-id="9d213-125">Uma árvore de Registro pode ter 512 níveis de profundidade.</span><span class="sxs-lookup"><span data-stu-id="9d213-125">A registry tree can be 512 levels deep.</span></span> <span data-ttu-id="9d213-126">Você pode criar até 32 níveis por vez por meio de uma única chamada à API do Registro.</span><span class="sxs-lookup"><span data-stu-id="9d213-126">You can create up to 32 levels at a time through a single registry API call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d213-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9d213-127">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9d213-128">[Visão geral do Registro do Windows](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="9d213-128">[Overview of the Windows Registry](/previous-versions/windows/it-pro/windows-server-2003/cc781906(v=ws.10))</span></span>
</dt> </dl>

 

 
