---
title: Função MpFreeMemory (MpClient. h)
description: Libera memória para o Gerenciador de proteção contra malware.
ms.assetid: D0B43AE5-756F-4E86-B8A5-8268A41901BC
keywords:
- Recursos do ambiente Windows herdado da função MpFreeMemory
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
ms.openlocfilehash: a15a2845b034a3aa739b1ba2f33a023b742b4b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644527"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**informações de MPRESOURCE \_**](mpresource-info.md)
</dt> <dt>

[**informações de MPTHREAT \_**](mpthreat-info.md)
</dt> <dt>

[**\_informações localizadas do MPTHREAT \_**](mpthreat-localized-info.md)
</dt> </dl>

 

 





