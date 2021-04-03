---
description: Contém informações usadas na criação de um contexto do Tablet.
ms.assetid: 10466c23-f4cb-4205-886b-d85a2f530afe
title: Estrutura de TABLET_CONTEXT_SETTINGS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TABLET_CONTEXT_SETTINGS
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9357281409ed4c48b4c6013a7a2be2997d58b094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922836"
---
# <a name="tablet_context_settings-structure"></a>Estrutura de configurações de \_ contexto do Tablet \_

Contém informações usadas na criação de um contexto do Tablet.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _TABLET_CONTEXT_SETTINGS {
  ULONG cPktProps;
  GUID  *pguidPktProps;
  ULONG cPktBtns;
  GUID  *pguidPktBtns;
  DWORD *pdwBtnDnMask;
  DWORD *pdwBtnUpMask;
  LONG  lXMargin;
  LONG  lYMargin;
} TABLET_CONTEXT_SETTINGS;
```



## <a name="members"></a>Membros

<dl> <dt>

**cPktProps**
</dt> <dd>

O número de propriedades em um pacote.

</dd> <dt>

**pguidPktProps**
</dt> <dd>

Identificadores exclusivos para as propriedades do pacote.

</dd> <dt>

**cPktBtns**
</dt> <dd>

O número de botões.

</dd> <dt>

**pguidPktBtns**
</dt> <dd>

Identificadores exclusivos para os botões.

</dd> <dt>

**pdwBtnDnMask**
</dt> <dd>

A máscara do botão para baixo.

</dd> <dt>

**pdwBtnUpMask**
</dt> <dd>

A máscara de botão para cima.

</dd> <dt>

**lXMargin**
</dt> <dd>

A margem de direção X.

</dd> <dt>

**lYMargin**
</dt> <dd>

A margem de direção Y.

</dd> </dl>

## <a name="remarks"></a>Comentários

Normalmente, um aplicativo obtém os valores padrão do [**método ITablet:: GetDefaultContextSettings**](itablet-getdefaultcontextsettings.md), modifica os valores para atender às suas necessidades e, em seguida, passa a estrutura de configurações modificada para o [**método ITablet:: CreateContext**](itablet-createcontext.md).

Essa estrutura determina quais eventos um aplicativo receberá, como eles serão processados e como eles serão entregues ao aplicativo ou ao próprio Windows.

As máscaras de botão, em conjunto, determinam quais tipos de eventos serão processados pelo contexto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                     |



 

 




