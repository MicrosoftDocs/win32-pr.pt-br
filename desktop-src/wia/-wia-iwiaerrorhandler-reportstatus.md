---
description: Lida com mensagens de erro e status durante transferências de dados de imagem e as exibe para o usuário.
ms.assetid: 23e85c63-80b9-4510-854d-289c8d23be2d
title: Método IWiaErrorHandler::ReportStatus (Wia.h)
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
ms.openlocfilehash: 6604dc8dbf0cad5f31449ff3cc30945c1e6059727d513fa98dbf436eb199f70f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659746"
---
# <a name="iwiaerrorhandlerreportstatus-method"></a>Método IWiaErrorHandler::ReportStatus

Lida com mensagens de erro e status durante transferências de dados de imagem e as exibe para o usuário.

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

*hwndParent* \[ Em\]
</dt> <dd>

Digite: **HWND**

**HWND** que é a janela pai da janela de mensagem.

</dd> <dt>

*queitem* \[ Em\]
</dt> <dd>

Tipo: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Ponteiro para a interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) do item que está sendo transferido. Esse objeto implementa minimamente [**IWiaItem2**](-wia-iwiaitem2.md) e [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).

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

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Retornará *hrStatus* se o erro não puder ser recuperado. Caso contrário, retornará um dos valores a seguir.



| Código de retorno                                                                             | Descrição                                                                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | A ação apropriada foi tomada para corrigir o erro e a transferência pode continuar. <br/> |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Nenhuma ação foi tomada para lidar com o erro ou o status do relatório para o usuário. <br/>                |
| <dl> <dt>**E \_ ABORT**</dt> </dl> | O usuário optou por anular a transferência em resposta à caixa de diálogo exibida. <br/>        |



 

## <a name="remarks"></a>Comentários

Windows A WIA (Aquisição de Imagem) 2.0 chama **IWiaErrorHandler::ReportStatus** quando o driver envia uma mensagem DE STATUS DO DISPOSITIVO **\_ DO MSG \_ \_** de IT para [**BandedDataCallback.**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback) Esse método trata a mensagem e exibe informações ao usuário sobre o status ou o erro. Se a mensagem for sobre um erro, o método permitirá que o usuário escolha, se possível, se deve tentar se recuperar do erro e continuar a transferência ou anular.

*hrStatus é* definido como WIA \_ STATUS TRANSFER BEGIN para informar ao manipulador que uma transferência foi \_ \_ iniciada. Ele é definido como WIA \_ STATUS TRANSFER END quando a transferência é \_ \_ concluída.

Se *hrStatus* for SEVERITY \_ SUCCESS, o usuário deverá ter permissão para cancelar a transferência.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
