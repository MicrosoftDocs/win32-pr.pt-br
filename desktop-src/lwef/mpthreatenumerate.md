---
title: Função MpThreatEnumerate (MpClient. h)
description: Retorna informações sobre a próxima ameaça na lista de enumeração. Essa função pode ser chamada repetidamente até que a enumeração de todas as ameaças seja concluída.
ms.assetid: 33244F4F-4FB7-4FA7-BC56-B9A30ABC3644
keywords:
- Recursos do ambiente Windows herdado da função MpThreatEnumerate
topic_type:
- apiref
api_name:
- MpThreatEnumerate
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acdbb7971371015a401c1a951ace8c55869fd405
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918816"
---
# <a name="mpthreatenumerate-function"></a>Função MpThreatEnumerate

Retorna informações sobre a próxima ameaça na lista de enumeração. Essa função pode ser chamada repetidamente até que a enumeração de todas as ameaças seja concluída.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI MpThreatEnumerate(
  _In_  MPHANDLE       hThreatEnumHandle,
  _Out_ PMPTHREAT_INFO *ppThreatInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hThreatEnumHandle* \[ no\]
</dt> <dd>

Tipo: **MPHANDLE**

Identificador para um contexto de enumeração de ameaça retornado por [**MpThreatOpen**](mpthreatopen.md).

</dd> <dt>

*ppThreatInfo* \[ fora\]
</dt> <dd>

Tipo: **PMPTHREAT \_ info \** _

Retorna um ponteiro para uma estrutura de informações de ameaça, [_ *MPTHREAT \_ info* *](mpthreat-info.md). A estrutura contém informações como ID de ameaça, nome e severidade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se a função for bem sucedido, o valor de retorno será **S \_ OK**.

Se não houver mais itens para retornar, o valor de retorno será **S \_ false**.

Se a função falhar, o valor de retorno será um código **HRESULT** com falha. O chamador pode usar a função [**MpErrorMessageFormat**](mperrormessageformat.md) para obter uma descrição genérica da mensagem de erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpThreatOpen**](mpthreatopen.md)
</dt> <dt>

[**informações de MPTHREAT \_**](mpthreat-info.md)
</dt> </dl>

 

 





