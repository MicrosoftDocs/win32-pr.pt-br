---
description: Retorna uma cadeia de caracteres que descreve o código de status.
ms.assetid: d3007f3e-46e1-4ab6-8ce3-c4e38f87ce61
title: Método IWiaErrorHandler::GetStatusDescription (Wia.h)
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
ms.openlocfilehash: 963dc0059cf4fd45dffb0fc406cb6b2849aef456309cf15e80bf094c2ce01d20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208298"
---
# <a name="iwiaerrorhandlergetstatusdescription-method"></a>Método IWiaErrorHandler::GetStatusDescription

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

*queitem* \[ Em\]
</dt> <dd>

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Ponteiro para [o IUnknown do](/windows/win32/api/unknwn/nn-unknwn-iunknown) item que está sendo transferido. Esse objeto implementa minimamente [**IWiaItem2**](-wia-iwiaitem2.md) e [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).

</dd> <dt>

*hrStatus* \[ Em\]
</dt> <dd>

Tipo: **HRESULT**

**HRESULT** que é o código de status recebido por [**BandedDataCallback.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)

</dd> <dt>

*cbResLength* \[ Em\]
</dt> <dd>

Tipo: **LONG**

**LONG** que é o tamanho dos dados referenciados por *pbData*.

</dd> <dt>

*pbData* \[ Em\]
</dt> <dd>

Tipo: **BYTE \***

Ponteiro para o buffer de dados conforme recebido por [**BandedDataCallback.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)

</dd> <dt>

*pbstrDescription* \[ out\]
</dt> <dd>

Tipo: **BSTR \***

**BSTR** que recebe uma descrição do status ou erro encontrado durante a transferência de dados. Esse parâmetro não pode ser **NULL.** O chamador deve liberar a cadeia de [caracteres usando SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)e o implementador deve alocar a cadeia de caracteres usando [SysAllocString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Retorna um dos valores a seguir.



| Código de retorno                                                                             | Descrição                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | *pbstrDescription contém* um ponteiro **BSTR** válido. <br/>  |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | *hrStatus* é desconhecido e nenhuma descrição está disponível. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
