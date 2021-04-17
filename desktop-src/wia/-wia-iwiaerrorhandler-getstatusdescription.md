---
description: Retorna uma cadeia de caracteres que descreve o código de status.
ms.assetid: d3007f3e-46e1-4ab6-8ce3-c4e38f87ce61
title: 'Método IWiaErrorHandler:: GetStatusDescription (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.GetStatusDescription
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: da23e413ee238f43ae577a51b18a542dc1b0768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797504"
---
# <a name="iwiaerrorhandlergetstatusdescription-method"></a>Método IWiaErrorHandler:: GetStatusDescription

Retorna uma cadeia de caracteres que descreve o código de status.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStatusDescription(
  [in]  IUnknown *punkItem,
  [in]  HRESULT  hrStatus,
  [in]  LONG     cbResLength,
  [in]  BYTE     *pbData,
  [out] BSTR     *pbstrDescription
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*punkItem* \[ no\]
</dt> <dd>

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Ponteiro para o [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) do item que está sendo transferido. Esse objeto implementa minimamente [_ *IWiaItem2* *](-wia-iwiaitem2.md) e [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).

</dd> <dt>

*hrStatus* \[ no\]
</dt> <dd>

Tipo: **HRESULT**

**HRESULT** que é o código de status recebido por [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).

</dd> <dt>

*cbResLength* \[ no\]
</dt> <dd>

Tipo: **longo**

**Longo** que é o tamanho dos dados referenciados por *pbData*.

</dd> <dt>

*pbData* \[ no\]
</dt> <dd>

Tipo: **byte \** _

Ponteiro para o buffer de dados como recebido por [_ *BandedDataCallback* *](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).

</dd> <dt>

*pbstrDescription* \[ fora\]
</dt> <dd>

Tipo: **BSTR \** _

_ *BSTR** que recebe uma descrição do status ou do erro encontrado durante a transferência de dados. Este parâmetro não pode ser **nulo**. O chamador deve liberar a cadeia de caracteres usando [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)e o implementador deve alocar a cadeia de caracteres usando [SysAllocString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Retorna um dos valores a seguir.



| Código de retorno                                                                             | Descrição                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | *pbstrDescription* contém um ponteiro **BSTR** válido. <br/>  |
| <dl> <dt>**\_falso**</dt> </dl> | *hrStatus* é desconhecido e nenhuma descrição está disponível. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
