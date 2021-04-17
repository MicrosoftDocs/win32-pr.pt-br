---
description: Exibe uma caixa de diálogo que permite ao usuário selecionar um dispositivo de hardware para aquisição de imagem.
ms.assetid: cd020dc6-fddf-4d7f-aa57-eae94953ef4e
title: 'Método IWiaDevMgr2:: SelectDeviceDlg (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: cb41ec8e94782ee4d7408c53e2d4e098d986fe83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812104"
---
# <a name="iwiadevmgr2selectdevicedlg-method"></a>Método IWiaDevMgr2:: SelectDeviceDlg

Exibe uma caixa de diálogo que permite ao usuário selecionar um dispositivo de hardware para aquisição de imagem.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SelectDeviceDlg(
  [in]          HWND      hwndParent,
  [in]          LONG      lDeviceType,
  [in]          LONG      lFlags,
  [in, out]     BSTR      *pbstrDeviceID,
  [out, retval] IWiaItem2 **ppItemRoot
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hwndParent* \[ no\]
</dt> <dd>

Tipo: **HWND**

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

*pbstrDeviceID* \[ entrada, saída\]
</dt> <dd>

Tipo: **BSTR \** _

Na saída, recebe uma cadeia de caracteres que contém a cadeia de caracteres do identificador do dispositivo. Na entrada, passe o endereço de um ponteiro se essas informações forem necessárias ou _ *NULL** se não for necessário.

</dd> <dt>

*ppItemRoot* \[ out, retval\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Recebe o endereço de um ponteiro para a interface [**IWiaItem2**](-wia-iwiaitem2.md) do item raiz da árvore hierárquica que representa o dispositivo WIA 2,0 selecionado. Se nenhum dispositivo for encontrado, ele receberá **NULL**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Esse método pode retornar um desses valores.



| Código de retorno                                                                                                  | Descrição                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | O dispositivo foi selecionado com êxito. <br/>                                                          |
| <dl> <dt>**\_falso**</dt> </dl>                      | O usuário cancelou a caixa de diálogo. <br/>                                                              |
| <dl> <dt>**WIA \_ S \_ nenhum \_ dispositivo \_ disponível**</dt> </dl> | Nenhum dispositivo de hardware WIA 2,0 corresponde às especificações fornecidas no parâmetro *lDeviceType* . <br/> |



 

## <a name="remarks"></a>Comentários

Esse método cria e exibe a caixa de diálogo **selecionar dispositivo** para que o usuário possa selecionar um dispositivo WIA 2,0 para aquisição de imagem. Se um dispositivo for selecionado com êxito, o método **IWiaDevMgr2:: SelectDeviceDlg** criará uma árvore hierárquica de objetos [**IWiaItem2**](-wia-iwiaitem2.md) para o dispositivo. Ele armazena um ponteiro para a interface **IWiaItem2** do item raiz no parâmetro *ppItemRoot*.

O aplicativo pode restringir os dispositivos exibidos ao usuário para tipos específicos especificando os tipos de dispositivo por meio do parâmetro *lDeviceType* . Se apenas um dispositivo atender à especificação, **IWiaDevMgr2:: SelectDeviceDlg** não exibirá a caixa de diálogo **selecionar dispositivo** . Em vez disso, ele cria a árvore [**IWiaItem2**](-wia-iwiaitem2.md) para o dispositivo e armazena um ponteiro para a interface **IWiaItem2** do item raiz no parâmetro *ppItemRoot*. Você pode substituir esse comportamento e forçar **IWiaDevMgr2:: SelectDeviceDlg** a exibir a caixa de diálogo ESPECIFICANDO o WIA \_ selecionar \_ dispositivo \_ como o valor para o parâmetro *lFlags* . Se mais de um dispositivo WIA 2,0 corresponder à especificação, todos os dispositivos correspondentes serão exibidos na caixa de diálogo **selecionar dispositivo** para que o usuário possa escolher um.

Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppItemRoot* .

> [!Note]  
> É recomendável que os aplicativos tornem a seleção de dispositivo e imagem disponível por meio de um item de menu chamado **de scanner** no menu **arquivo** .

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
