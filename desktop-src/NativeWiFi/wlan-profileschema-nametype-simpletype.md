---
description: Conter o nome ou uma descrição de um perfil de LAN sem fio.
ms.assetid: cb30d76f-051f-4b90-a0e0-24088a99ca9b
title: Tipo simples nametype (LAN_policy) (perfil)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- nameType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e73e8bd013836767e2a943616407aea9f563fea2
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187831"
---
# <a name="nametype-simple-type-lan_policy-for-profileschema"></a><span data-ttu-id="87416-103">Tipo simples nametype (LAN_policy) para profileschema</span><span class="sxs-lookup"><span data-stu-id="87416-103">nameType Simple Type (LAN_policy) for profileschema</span></span>

<span data-ttu-id="87416-104">O tipo simples nametype pode conter o nome ou uma descrição de um perfil de LAN sem fio.</span><span class="sxs-lookup"><span data-stu-id="87416-104">The nameType simple type can contain either the name or a description of a wireless LAN profile.</span></span> <span data-ttu-id="87416-105">Esse valor de cadeia de caracteres deve ter entre 1 e 255 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="87416-105">This string value must be between 1 and 255 characters long.</span></span>

``` syntax
<xs:simpleType name="nameType">
    <xs:restriction
        base="string"
    >
        <xs:minLength
            value="1"
         />
        <xs:maxLength
            value="255"
         />
    </xs:restriction>
</xs:simpleType>
```

## <a name="requirements"></a><span data-ttu-id="87416-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87416-106">Requirements</span></span>



| <span data-ttu-id="87416-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="87416-107">Requirement</span></span> | <span data-ttu-id="87416-108">Valor</span><span class="sxs-lookup"><span data-stu-id="87416-108">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="87416-109">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87416-109">Minimum supported client</span></span><br/> | <span data-ttu-id="87416-110">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP3\]</span><span class="sxs-lookup"><span data-stu-id="87416-110">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="87416-111">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87416-111">Minimum supported server</span></span><br/> | <span data-ttu-id="87416-112">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="87416-112">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="87416-113">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="87416-113">Redistributable</span></span><br/>          | <span data-ttu-id="87416-114">API de LAN sem fio para Windows XP com SP2</span><span class="sxs-lookup"><span data-stu-id="87416-114">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



 

 




