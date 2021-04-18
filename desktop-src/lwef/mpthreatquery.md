---
title: Função MpThreatQuery (MpClient. h)
description: Usado para consultar informações estáticas (como severidade e categoria) ou localizadas (como descrição da categoria e conselhos) sobre uma determinada ameaça.
ms.assetid: A06854B2-8444-46A4-A53F-FD5FEAFF47B7
keywords:
- Recursos do ambiente Windows herdado da função MpThreatQuery
topic_type:
- apiref
api_name:
- MpThreatQuery
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d38a3734f9d98f3bd61143d4fe58bd606c7508
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757178"
---
# <a name="mpthreatquery-function"></a>Função MpThreatQuery

Usado para consultar informações estáticas (como severidade e categoria) ou localizadas (como descrição da categoria e conselhos) sobre uma determinada ameaça.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI MpThreatQuery(
  _In_      MPHANDLE                 hMpHandle,
  _In_      MPTHREAT_ID              ThreatID,
  _Out_     PMPTHREAT_INFO           *ppThreatInfo,
  _Out_opt_ PMPTHREAT_LOCALIZED_INFO *ppThreatLocalizedInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hMpHandle* \[ no\]
</dt> <dd>

Tipo: **MPHANDLE**

Identificador para a interface do Malware Protection Manager. Esse identificador é retornado pela função [**MpManagerOpen**](mpmanageropen.md) .

</dd> <dt>

*Threatid* \[ no\]
</dt> <dd>

Tipo: **\_ ID de MPTHREAT**

Identificador de ameaça para o qual as informações são solicitadas.

</dd> <dt>

*ppThreatInfo* \[ fora\]
</dt> <dd>

Tipo: **PMPTHREAT \_ info \** _

Retorna um ponteiro para uma estrutura de informações de ameaça, [_ *MPTHREAT \_ info* *](mpthreat-info.md). A estrutura contém informações como ID de ameaça, nome e severidade.

</dd> <dt>

*ppThreatLocalizedInfo* \[ out, opcional\]
</dt> <dd>

Tipo: **PMPTHREAT \_ \_ informações \* localizadas* _

Retorna um ponteiro para uma estrutura que contém informações localizadas sobre a ameaça. Você pode passar _ *NULL** se não estiver interessado em informações localizadas sobre a ameaça. Consulte [**\_ informações localizadas \_ sobre o MPTHREAT**](mpthreat-localized-info.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se a função for bem sucedido, o valor de retorno será **S \_ OK**.

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

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**informações de MPTHREAT \_**](mpthreat-info.md)
</dt> <dt>

[**\_informações localizadas do MPTHREAT \_**](mpthreat-localized-info.md)
</dt> </dl>

 

 





