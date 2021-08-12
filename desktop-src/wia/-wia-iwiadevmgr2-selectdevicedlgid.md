---
description: 'Método IWiaDevMgr2:: SelectDeviceDlgID – exibe uma caixa de diálogo que permite ao usuário selecionar um dispositivo de hardware para aquisição de imagem.'
ms.assetid: 6baca959-0f97-4a39-88d0-ed34b813c80a
title: 'Método IWiaDevMgr2:: SelectDeviceDlgID (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlgID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 95b5134a2c7f7411ffcf2860f8829225a7271089c824b4e4c8731de78ffa4a61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118440798"
---
# <a name="iwiadevmgr2selectdevicedlgid-method"></a>Método IWiaDevMgr2:: SelectDeviceDlgID

Exibe uma caixa de diálogo que permite ao usuário selecionar um dispositivo de hardware para aquisição de imagem.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SelectDeviceDlgID(
  [in]          HWND hwndParent,
  [in]          LONG lDeviceType,
  [in]          LONG lFlags,
  [out, retval] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndParent* \[ no\]
</dt> <dd>

Digite: **HWND**

Especifica a janela pai da caixa de diálogo **selecionar dispositivo** .

</dd> <dt>

*lDeviceType* \[ no\]
</dt> <dd>

Tipo: **longo**

Especifica o tipo de dispositivo WIA 2,0 a ser usado. Consulte [especificadores de tipo de dispositivo WIA](-wia-wia-device-type-specifiers.md) para obter uma lista de valores possíveis.

</dd> <dt>

*lFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Especifica o comportamento da caixa de diálogo. O valor pode ser um dos seguintes.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Use o comportamento padrão.

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA \_ selecionar \_ dispositivo \_ padrão**


</dt> <dd>

Exibir a caixa de diálogo mesmo que haja apenas um dispositivo correspondente.

</dd> </dl> </dd> <dt>

*pbstrDeviceID* \[ out, retval\]
</dt> <dd>

Tipo: **BSTR \***

Ponteiro para uma cadeia de caracteres que recebe a cadeia de caracteres do identificador do dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Esse método pode retornar um desses valores.



| Código de retorno                                                                                                  | Descrição                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | O dispositivo foi selecionado com êxito. <br/>                                                          |
| <dl> <dt>**\_falso**</dt> </dl>                      | O usuário cancelou a caixa de diálogo. <br/>                                                              |
| <dl> <dt>**WIA \_ S \_ nenhum \_ dispositivo \_ disponível**</dt> </dl> | Nenhum dispositivo de hardware WIA 2,0 corresponde às especificações fornecidas no parâmetro *lDeviceType* . <br/> |



 

## <a name="remarks"></a>Comentários

Esse método cria e exibe a caixa de diálogo **selecionar dispositivo** para que o usuário possa selecionar um dispositivo WIA 2,0 para aquisição de imagem. Se um dispositivo for selecionado com êxito, o método **IWiaDevMgr2:: SelectDeviceDlgID** passará sua cadeia de caracteres de identificador para o aplicativo por meio de seu parâmetro *pbstrDeviceID* .

O aplicativo pode restringir os dispositivos exibidos ao usuário para tipos específicos especificando os tipos de dispositivo por meio do parâmetro *lDeviceType* . Se apenas um dispositivo atender à especificação, **IWiaDevMgr2:: SelectDeviceDlgID** não exibirá a caixa de diálogo **selecionar dispositivo** . Em vez disso, ele passa a cadeia de caracteres do identificador do dispositivo para o aplicativo sem exibir a caixa de diálogo. Você pode substituir esse comportamento e forçar **IWiaDevMgr2:: SelectDeviceDlgID** a exibir a caixa de diálogo passando o \_ WIA \_ selecione \_ o dispositivo como o valor para o parâmetro *lFlags* . Se mais de um dispositivo WIA 2,0 corresponder à especificação, todos os dispositivos correspondentes serão exibidos na caixa de diálogo SelectDevice para que o usuário possa escolher um.

> [!Note]  
> É recomendável que os aplicativos tornem a seleção de dispositivo e imagem disponível por meio de um item de menu chamado **de scanner** no menu **arquivo** .

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




