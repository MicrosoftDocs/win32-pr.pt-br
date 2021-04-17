---
title: Suporte à linguagem XML
description: Esta seção descreve o nível de suporte à linguagem XML no WWS.
ms.assetid: c3408c2a-6506-4a2e-8083-b4a0154a6918
keywords:
- Serviços Web de suporte de linguagem XML para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a13425d2ed9c878c3a63dd5b5908ffbab4f2f177
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "105750875"
---
# <a name="xml-language-support"></a><span data-ttu-id="40704-106">Suporte à linguagem XML</span><span class="sxs-lookup"><span data-stu-id="40704-106">XML Language Support</span></span>

<span data-ttu-id="40704-107">Esta seção descreve o nível de suporte à linguagem XML no WWS.</span><span class="sxs-lookup"><span data-stu-id="40704-107">This section describe level of XML Language support in WWS.</span></span>


<span data-ttu-id="40704-108">Consulte as funções DownlevelLCIDToLocaleName em versões do Windows anteriores ao Windows Vista e LCIDToLocalName, caso contrário, para converter entre um LCID e um valor XML: lang.</span><span class="sxs-lookup"><span data-stu-id="40704-108">See the functions DownlevelLCIDToLocaleName on versions of Windows earlier than Windows Vista, and LCIDToLocalName otherwise, to convert between an LCID and an xml:lang value.</span></span>

<span data-ttu-id="40704-109">Ao ler, [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute) pode ser usado para descobrir o valor de um atributo "XML: lang" no escopo.</span><span class="sxs-lookup"><span data-stu-id="40704-109">When reading, [**WsGetXmlAttribute**](/windows/desktop/api/WebServices/nf-webservices-wsgetxmlattribute) may be used to discover the value of an "xml:lang" attribute in scope.</span></span>

<span data-ttu-id="40704-110">Durante a gravação, [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute) pode ser usado para gravar um atributo "XML: lang".</span><span class="sxs-lookup"><span data-stu-id="40704-110">When writing, [**WsWriteStartAttribute**](/windows/desktop/api/WebServices/nf-webservices-wswritestartattribute) may be used to write an "xml:lang" attribute.</span></span>

 

 




