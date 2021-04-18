---
description: Manipula mensagens de status e de erro durante transferências de dados de imagem e as exibe para o usuário.
ms.assetid: 23e85c63-80b9-4510-854d-289c8d23be2d
title: 'Método IWiaErrorHandler:: ReportStatus (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 30a082502d4c7bc5b789fd1ec19fdb76f63d8fab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756662"
---
# <a name="iwiaerrorhandlerreportstatus-method"></a>Método IWiaErrorHandler:: ReportStatus

Manipula mensagens de status e de erro durante transferências de dados de imagem e as exibe para o usuário.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReportStatus(
  [in] HWND     hwndParent,
  [in] IUnknown *punkItem,
  [in] HRESULT  hrStatus,
  [in] LONG     cbResLength,
  [in] BYTE     *pbData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndParent* \[ no\]
</dt> <dd>

Tipo: **HWND**

**HWND** que é a janela pai da janela de mensagem.

</dd> <dt>

*punkItem* \[ no\]
</dt> <dd>

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _

Ponteiro para a interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) do item que está sendo transferido. Esse objeto implementa minimamente [_ *IWiaItem2* *](-wia-iwiaitem2.md) e [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).

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

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Retorna *hrStatus* se o erro não puder ser recuperado de. Caso contrário, ele retorna um dos valores a seguir.



| Código de retorno                                                                             | Descrição                                                                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | A ação apropriada foi tomada para corrigir o erro e a transferência pode continuar. <br/> |
| <dl> <dt>**\_falso**</dt> </dl> | Nenhuma ação foi tomada para manipular o erro ou o status do relatório para o usuário. <br/>                |
| <dl> <dt>**E \_ anular**</dt> </dl> | O usuário optou por anular a transferência em resposta à caixa de diálogo exibida. <br/>        |



 

## <a name="remarks"></a>Comentários

O WIA (Windows Image Acquisition) 2,0 chama **IWiaErrorHandler:: ReportStatus** quando o driver envia uma mensagem de **\_ \_ \_ status do dispositivo msg de ti** para [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback). Esse método manipula a mensagem e exibe informações para o usuário sobre o status ou o erro. Se a mensagem for sobre um erro, o método permitirá que o usuário escolha, se possível, se deseja tentar se recuperar do erro e continuar a transferência ou para anular.

*hrStatus* é definido como a \_ transferência de status \_ do WIA \_ comece a informar ao manipulador que uma transferência foi iniciada. Ele é definido como \_ \_ \_ término da transferência de status do WIA quando a transferência é concluída.

Se *hrStatus* for \_ êxito na gravidade, o usuário deverá ter permissão para cancelar a transferência.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
