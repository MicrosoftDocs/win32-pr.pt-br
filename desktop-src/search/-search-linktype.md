---
description: Especifica o tipo de link ao rastrear ou indexar.
ms.assetid: 2a0ddb31-df35-4da5-9950-b091cd461556
title: Enumeração de LINKID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LINKTYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 16c61f8d92a6f90be0fa4b64ddd9d582987ac0bdf52ca1c596c7db3a7fa4b669
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118463039"
---
# <a name="linktype-enumeration"></a>Enumeração de LINKID

\[a enumeração **linkid** só tem suporte no Windows XP e no Windows Server 2003 e não deve mais ser usada.\]

Especifica o tipo de link ao rastrear ou indexar.

## <a name="syntax"></a>Syntax


```C++
typedef enum _LINKTYPE { 
  LINKTYPE_URL      = 0x00000000,
  LINKTYPE_CONTENT  = 0x00000001,
  LINKTYPE_RELATED  = 0x00000002
} LINKTYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="LINKTYPE_URL"></span><span id="linktype_url"></span>**URL de LINKID \_**
</dt> <dd>

Especifica se o tipo de link de URLs deve ser indexado.

</dd> <dt>

<span id="LINKTYPE_CONTENT"></span><span id="linktype_content"></span>**conteúdo de LINKtype \_**
</dt> <dd>

Especifica se o conteúdo do link deve ser indexado.

</dd> <dt>

<span id="LINKTYPE_RELATED"></span><span id="linktype_related"></span>**LINKtype \_ relacionado**
</dt> <dd>

Especifica um link relacionado.

</dd> </dl>

## <a name="remarks"></a>Comentários

para visualizar os anexos com um manipulador de protocolo de terceiros em computadores que executam o Windows XP ou o Windows Server 2003, pode ser necessário usar os sinalizadores **linkid** e as outras APIs a seguir: os métodos [**IItemPreviewerExt:: GetLinkedContent**](-search-iitempreviewerext-getlinkedcontent.md) e [**IItemPreviewerExt:: GetRelatedPart**](-search-iitempreviewerext-getrelatedpart.md) e a estrutura [**LINKINFO**](-search-linkinfo.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos de área de trabalho do SP2\]<br/> |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/> |



 

 




