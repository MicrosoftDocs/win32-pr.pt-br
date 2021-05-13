---
description: Usado para determinar se um item está presente em uma lista de MRU (usado mais recentemente).
title: Função de retorno de chamada MRUCMPPROC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MRUCMPPROC
- MRUCMPPROCA
- MRUCMPPROCW
api_type:
- UserDefined
api_location: ''
ms.assetid: 00f31d6b-2a96-4abd-9647-24a6e66aa22f
ms.openlocfilehash: 83020fbcd0d4cfcfbc643d1360e3671595de6f32
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840777"
---
# <a name="mrucmpproc-callback-function"></a>Função de retorno de chamada MRUCMPPROC

Usado para determinar se um item está presente em uma lista de MRU (usado mais recentemente).

## <a name="syntax"></a>Sintaxe


```C++
int CALLBACK MRUCMPPROC(
   LPCTSTR pString1,
   LPCTSTR pString2
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pString1* 
</dt> <dd>

Tipo: **LPCTSTR**

A primeira cadeia de caracteres.

</dd> <dt>

*pString2* 
</dt> <dd>

Tipo: **LPCTSTR**

Uma segunda cadeia de caracteres para comparar com a primeira.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **int**

Retornará 0 se os itens forem idênticos, caso contrário, um valor diferente de zero.

## <a name="remarks"></a>Comentários

Essa função pode ser especificada opcionalmente para uso na estrutura [**MRUINFO**](mruinfo.md) passada para [**CreateMRUListW**](createmrulist.md). Isso é útil quando a lista MRU foi criada com o **sinalizador \_ binário MRU** . Quando essa função não é especificada, as funções de comparação de cadeia de caracteres padrão são usadas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>      |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>            |
| Nomes Unicode e ANSI<br/>   | **MRUCMPPROCW** (Unicode) e **MRUCMPPROCA** (ANSI)<br/> |



 

 




