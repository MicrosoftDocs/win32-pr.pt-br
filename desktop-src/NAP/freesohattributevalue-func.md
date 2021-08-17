---
title: Função FreeSoHAttributeValue (NapUtil.h)
description: Libera uma estrutura de dados SoHAttributeValue.
ms.assetid: 21647ee6-2ea2-45fd-b1f2-fb1836196f94
keywords:
- Função FreeSoHAttributeValue NAP
topic_type:
- apiref
api_name:
- FreeSoHAttributeValue
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 877a333c7eb43c3921c7727bcc15a958bdcd2565fabe4636a67868f3a27bf473
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940400"
---
# <a name="freesohattributevalue-function"></a>Função FreeSoHAttributeValue

> [!Note]  
> A plataforma de Proteção de Acesso à Rede não está disponível a partir do Windows 10

 

A **função FreeSoHAttributeValue** libera uma estrutura de dados [**SoHAttributeValue.**](sohattributevalue-union.md)

## <a name="syntax"></a>Sintaxe


```C++
NAPAPI VOID WINAPI FreeSoHAttributeValue(
  _In_ SoHAttributeType  type,
  _In_ SoHAttributeValue *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*tipo* \[ Em\]
</dt> <dd>

Um [**valor SoHAttributeType**](sohattributetype-enum.md) que especifica o tipo de valor do atributo SoH a ser liberado.

</dd> <dt>

*value* \[ Em\]
</dt> <dd>

Um ponteiro para [**SoHAttributeValue**](sohattributevalue-union.md) a ser liberado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Todas as interfaces COM com suporte pelo sistema NAP usam regras de gerenciamento de memória COM padrão e alocadores de memória COM (**CoTaskMemAlloc** e **CoTaskMemFree**):

-   **Em,** os parâmetros são alocados e liberados pelo chamador.
-   **Os** parâmetros out são alocados pelo chamador e liberados pelo chamador usando **CoTaskMem.**
-   **Os parâmetros** de saída são alocados pelo chamador, liberados e realocados pelo chamador e, por fim, liberados pelo chamador, usando **CoTaskMem.**

Todas as funções NAP para liberar memória também liberam todos os ponteiros inseridos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



 

 





