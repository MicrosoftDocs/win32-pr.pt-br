---
description: A interface IWiaItem2 fornece aplicativos com a mesma funcionalidade que a interface IWiaItem (a capacidade de consultar dispositivos para descobrir seus recursos, acessar interfaces de transferência de dados e propriedades de item e controlar o dispositivo).
ms.assetid: 4e29ea54-1ee7-4150-b26c-f8c7f41a3f08
title: Interface IWiaItem2 (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2150b726e6dcdfdeb150de48c78a7a0b2f2ee3e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827169"
---
# <a name="iwiaitem2-interface"></a>Interface IWiaItem2

A interface **IWiaItem2** fornece aplicativos com a mesma funcionalidade que a interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (a capacidade de consultar dispositivos para descobrir seus recursos, acessar interfaces de transferência de dados e propriedades de item e controlar o dispositivo). Ele também fornece ao aplicativo a capacidade de criar e usar dinamicamente filtros de processamento de imagens que podem vir como extensões dos drivers de dispositivo do WIA (Windows Image Acquisition) 2,0 fornecidos no Windows Vista.

## <a name="members"></a>Membros

A interface **IWiaItem2** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaItem2** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWiaItem2** tem esses métodos.



| Método                                                                  | Descrição                                                                                                                                                                                                  |
|:------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CheckExtension**](-wia-iwiaitem2-checkextension.md)                 | Verifica se uma extensão especificada está disponível no computador e pode ser usada pelo método [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md) . <br/>                                   |
| [**Createchilditem**](-wia-iwiaitem2-createchilditem.md)               | Crie um novo item filho. Adiciona objetos **IWiaItem2** à árvore **IWiaItem2** do dispositivo. <br/>                                                                                                            |
| [**DeleteItem**](-wia-iwiaitem2-deleteitem.md)                         | Remove o objeto **IWiaItem2** atual da árvore de objetos do dispositivo. <br/>                                                                                                                          |
| [**DeviceCommand**](-wia-iwiaitem2-devicecommand.md)                   | Emite um comando para um dispositivo de hardware WIA 2,0. <br/>                                                                                                                                                   |
| [**DeviceDlg**](-wia-iwiaitem2-devicedlg.md)                           | Exibe uma caixa de diálogo para o usuário se preparar para a aquisição de imagem. <br/>                                                                                                                              |
| [**DPS**](-wia-iwiaitem2-diagnostic.md)                         | Não há suporte no momento.<br/>                                                                                                                                                                          |
| [**EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)                 | Cria um objeto enumerador e passa de volta um ponteiro para sua interface [**IEnumWiaItem2**](-wia-ienumwiaitem2.md) para pastas com itens na árvore **IWiaItem2** de um dispositivo WIA 2,0. <br/>        |
| [**EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) | Cria um enumerador que é usado para verificar os comandos e eventos aos quais um dispositivo WIA 2,0 dá suporte. <br/>                                                                                               |
| [**EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md)   | O método [**IWiaItem2:: EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) cria um enumerador usado para obter informações sobre eventos para os quais um aplicativo é registrado.<br/> |
| [**FindItemByName**](-wia-iwiaitem2-finditembyname.md)                 | Pesquisa a árvore de subitens de um item usando o nome como a chave de pesquisa. <br/>                                                                                                                            |
| [**GetExtension**](-wia-iwiaitem2-getextension.md)                     | Obtém as interfaces de extensão que podem vir com um driver de dispositivo WIA 2,0. <br/>                                                                                                                      |
| [**GetItemCategory**](-wia-iwiaitem2-getitemcategory.md)               | Obtém as informações de categoria de um item. <br/>                                                                                                                                                             |
| [**GetItemType**](-wia-iwiaitem2-getitemtype.md)                       | Obtém as informações de tipo de um item. <br/>                                                                                                                                                                 |
| [**GetParentItem**](-wia-iwiaitem2-getparentitem.md)                   | Obtém o item pai na árvore que representa um dispositivo de hardware WIA 2,0. <br/>                                                                                                                      |
| [**GetPreviewComponent**](-wia-iwiaitem2-getpreviewcomponent.md)       | Obtém o componente de visualização do WIA 2,0.<br/>                                                                                                                                                               |
| [**GetRootItem**](-wia-iwiaitem2-getrootitem.md)                       | Obtém o item raiz de uma árvore de objetos de item usados para representar um dispositivo de hardware WIA 2,0. <br/>                                                                                                        |



 

## <a name="remarks"></a>Comentários

A árvore de itens do WIA 2,0 que um aplicativo pode ver é separada da árvore que é criada e mantida por uma minidriver WIA 2,0. Quando um minidriver cria uma árvore de itens, o serviço WIA 2,0 usa essa árvore de itens WIA 2,0 como um guia para criar cópias idênticas que podem ser exibidas por aplicativos de geração de imagens. Os itens na árvore copiada são chamados de itens de aplicativo. Os itens na árvore criados por um minidriver são chamados de itens de driver. No Windows Vista, as árvores de itens WIA 2,0 são criadas de objetos **IWiaItem2** , cada um dos quais implementa a interface **IWiaItem2** ).

A interface **IWiaItem2** , como todas as interfaces de Component Object Model (com), herda os métodos de interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



| Métodos IUnknown                                        | Descrição                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Retorna ponteiros para interfaces com suporte. |
| [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa a contagem de referência.               |
| [IUnknown:: versão](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Decrementa a contagem de referência.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
