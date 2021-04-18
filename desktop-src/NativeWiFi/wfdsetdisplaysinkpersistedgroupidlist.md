---
description: Define a lista de IDs de grupo persistente para todos os perfis que são persistidos por seu aplicativo.
ms.assetid: EF83F295-CD53-45A4-B209-560B4069CA7C
title: Função WFDDisplaySinkSetPersistedGroupIDList (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDSetDisplaySinkPersistedGroupIDList
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423360d7127f331fd1aa2de7f7370daebcc2b417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753138"
---
# <a name="wfddisplaysinksetpersistedgroupidlist-function"></a>Função WFDDisplaySinkSetPersistedGroupIDList

Define a lista de IDs de grupo persistente para todos os perfis que são persistidos por seu aplicativo. Seu aplicativo deve chamar esse método toda vez que adicionar ou excluir um perfil de seu armazenamento.

## <a name="syntax"></a>Sintaxe


```C++
DWORD WINAPI WFDSetDisplaySinkPersistedGroupIDList(
  _In_ UINT32             cGroupIDList,
  _In_ DOT11_WFD_GROUP_ID *pGroupIDList
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cGroupIDList* \[ no\]
</dt> <dd>

A contagem de IDs de grupo que está sendo apontada por *pGroupIDList*.

</dd> <dt>

*pGroupIDList* \[ no\]
</dt> <dd>

Ponteiro para uma matriz de IDs de grupo *cGroupIDList* .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será \_ êxito no erro.

## <a name="remarks"></a>Comentários

Esse método sempre deve ser chamado com a lista inteira e não um subconjunto. OK para chamar esse método com 0 perfis quando o repositório de perfis estiver vazio.

Uma reinvocação para uma ID de grupo que não faz parte da lista fornecida falhará com "falha; Grupo P2P desconhecido "(status 8).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                    |
| Fim do suporte do cliente<br/>    | Windows 10<br/>                                                                      |
| Fim do suporte do servidor<br/>    | Windows Server 2016<br/>                                                             |
| parâmetro<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Wifidisplay. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



 

 




