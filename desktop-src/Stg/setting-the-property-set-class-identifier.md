---
title: Definindo o identificador de classe do conjunto de propriedades
description: O método SetClass IPropertyStorage define o CLSID do objeto de armazenamento e o valor da marca de classe armazenados no conjunto de propriedades COM. Isso ocorre quando invocado em um armazenamento de propriedade não simples armazenado em um objeto de armazenamento estruturado.
ms.assetid: 3f542a66-5e04-43c1-a386-7d709c615972
keywords:
- Definindo o identificador de classe do conjunto de propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9ec6e038ef6bc5f4f12228581946a4051c532b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005959"
---
# <a name="setting-the-property-set-class-identifier"></a><span data-ttu-id="223cf-105">Definindo o identificador de classe do conjunto de propriedades</span><span class="sxs-lookup"><span data-stu-id="223cf-105">Setting the Property Set Class Identifier</span></span>

<span data-ttu-id="223cf-106">O método [**IPropertyStorage:: SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass) define o CLSID do objeto de armazenamento e o valor da marca de classe armazenados no conjunto de propriedades com.</span><span class="sxs-lookup"><span data-stu-id="223cf-106">The [**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass) method sets both the CLSID of the storage object and the class tag value stored in the COM property set.</span></span> <span data-ttu-id="223cf-107">Isso ocorre quando invocado em um armazenamento de propriedade não simples armazenado em um objeto de armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="223cf-107">This occurs when invoked on a nonsimple property storage stored in a structured storage object.</span></span>

<span data-ttu-id="223cf-108">Isso fornece consistência e uniformidade que cria uma melhor interação com algumas ferramentas.</span><span class="sxs-lookup"><span data-stu-id="223cf-108">This provides consistency and uniformity which creates better interaction with some tools.</span></span> <span data-ttu-id="223cf-109">Um objeto de armazenamento de propriedade é não simples se for criado chamando [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) com o sinalizador de **PROPSETFLAG não \_ simples** definido.</span><span class="sxs-lookup"><span data-stu-id="223cf-109">A property storage object is nonsimple if it is created by calling [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) with the **PROPSETFLAG\_NONSIMPLE** flag set.</span></span>

<span data-ttu-id="223cf-110">O CLSID do objeto de armazenamento é definido com uma chamada para [**IStorage:: SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass).</span><span class="sxs-lookup"><span data-stu-id="223cf-110">The CLSID of the storage object is set with a call to [**IStorage::SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass).</span></span>

 

 




