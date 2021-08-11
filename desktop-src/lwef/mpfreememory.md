---
title: Função MpFreeMemory (MpClient. h)
description: Libera memória para o Gerenciador de proteção contra malware.
ms.assetid: D0B43AE5-756F-4E86-B8A5-8268A41901BC
keywords:
- recursos de ambiente de Windows herdado da função MpFreeMemory
topic_type:
- apiref
api_name:
- MpFreeMemory
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 806795cee45fcfe95473c0961106da074c1157b65ac5c19f5d4813c84865616a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247421"
---
# <a name="mpfreememory-function"></a>Função MpFreeMemory

Libera memória para o Gerenciador de proteção contra malware. Todos os buffers alocados e retornados pelas funções de proteção contra malware devem ser liberados pelo chamador usando essa função.

## <a name="syntax"></a>Sintaxe


```C++
void WINAPI MpFreeMemory(
  _In_ PVOID pMemory
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pMemory* \[ no\]
</dt> <dd>

Tipo: **pVoid**

Um ponteiro para a memória alocada por uma função de proteção contra malware.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função não retorna um valor.

## <a name="remarks"></a>Comentários

Para facilitar o gerenciamento de memória para clientes, o Malware Protection Manager também define macros para liberar memória associada a várias estruturas retornadas pelas funções de proteção contra malware. As macros a seguir são definidas no arquivo de cabeçalho mpmemfree. h:



| Name                            | Descrição                                                                      |
|---------------------------------|----------------------------------------------------------------------------------|
| \_informações \_ gratuitas do MPRESOURCE          | Libera uma [**\_ informação MPRESOURCE**](mpresource-info.md)alocada.                  |
| \_informações \_ gratuitas do MPTHREAT            | Libera uma [**\_ informação MPTHREAT**](mpthreat-info.md)alocada.                      |
| \_informações localizadas do MPTHREAT \_ \_ gratuito | Libera uma [**\_ \_ informação localizada de MPTHREAT**](mpthreat-localized-info.md)alocada. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**informações de MPRESOURCE \_**](mpresource-info.md)
</dt> <dt>

[**informações de MPTHREAT \_**](mpthreat-info.md)
</dt> <dt>

[**\_informações localizadas do MPTHREAT \_**](mpthreat-localized-info.md)
</dt> </dl>

 

 





