---
description: A interface IWiaImageFilter é uma interface de extensão implementada por desenvolvedores de filtro de processamento de imagens e chamada pelo WIA (Windows Image Acquisition) 2,0.
ms.assetid: 2abe913b-bb2b-486d-a3f4-d5932433fc82
title: Interface IWiaImageFilter (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaImageFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 8d859b79d15db627bb09cb60f758791a8b5860f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828450"
---
# <a name="iwiaimagefilter-interface"></a>Interface IWiaImageFilter

A interface **IWiaImageFilter** é uma interface de extensão implementada por desenvolvedores de filtro de processamento de imagens e chamada pelo WIA (Windows Image Acquisition) 2,0.

## <a name="members"></a>Membros

A interface **IWiaImageFilter** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaImageFilter** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWiaImageFilter** tem esses métodos.



| Método                                                                | Descrição                                                                                             |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**Aplicarproperties**](-wia-iwiaimagefilter-applyproperties.md)       | Permite que o filtro de processamento de imagens grave Propriedades de volta para o driver (e dispositivo).<br/>     |
| [**FilterPreviewImage**](-wia-iwiaimagefilter-filterpreviewimage.md) | Filtra a imagem de visualização.<br/>                                                                   |
| [**InitializeFilter**](-wia-iwiaimagefilter-initializefilter.md)     | Inicializa o filtro. Chamado pelo WIA 2,0 antes de cada download de imagem. <br/>                       |
| [**SetNewCallback**](-wia-iwiaimagefilter-setnewcallback.md)         | Define um novo retorno de chamada de aplicativo para o filtro de processamento de imagem a ser usado para chamadas de encaminhamento.<br/> |



 

## <a name="remarks"></a>Comentários

Os desenvolvedores de filtro de processamento de imagens devem implementar essa interface e a interface [**IWiaTransferCallback**](-wia-iwiatransfercallback.md) .

WIA 2,0 chama métodos de filtro. Eles nunca são chamados diretamente de um aplicativo.

A Microsoft fornece o componente de visualização do WIA 2,0, que armazena em cache a imagem de visualização original e não filtrada que é adquirida do verificador. Um aplicativo usa [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) para criar uma instância do componente de visualização do WIA 2,0 (CLSID \_ WiaPreview), que carrega o filtro usando [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md). O filtro é chamado automaticamente quando o aplicativo chama [**IWiaTransfer::D aixar**](-wia-iwiatransfer-download.md).

O filtro de processamento de imagens sempre é executado quando uma imagem é verificada. Um aplicativo não pode adquirir uma imagem do scanner sem ter o filtro de geração de imagens aplicado primeiro.

Um filtro deve implementar o brilho e o contraste no mínimo. A interface de usuário comum, que fornece controles de brilho e contraste para o usuário, pode exibir visualizações precisas para o usuário.

Um filtro de processamento de imagem nunca deve modificar o membro *lMessage* da estrutura [**WiaTransferParams**](-wia-wiatransferparams.md) .

Para ler as propriedades necessárias, o filtro de processamento de imagem deve chamar [**IWiaPropertyStorage:: GetPropertyStream**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiapropertystorage-getpropertystream) na interface [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) obtida do item chamando [IWiaImageFilter:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). Em seguida, o filtro pode instanciar uma instância de [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) nesse fluxo para ler as propriedades de itens. O filtro de processamento de imagem não deve chamar [IWiaPropertyStorage:: ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) diretamente porque esse método chama o driver `drvReadItemProperties` , mas o serviço WIA 2,0 já bloqueou o driver na `drvAcquireItemData` chamada para que essa chamada se limite e falhe.

As propriedades das quais o filtro está interessado podem, por exemplo, ser as configurações de brilho e contraste. Normalmente, o filtro também precisa ler o formato da imagem, bem como a propriedade Preview, a [**\_ \_ visualização do DPS do WIA**](-wia-wiaitempropscannerdevice.md), de *pWiaItem2*. Essas propriedades são todas usadas no processo de filtragem.

Os componentes WIA 2,0 sempre gravam dados não filtrados no filtro de processamento de imagens. O algoritmo de processamento de imagem implementado pelo fluxo do filtro pode filtrar os dados mais de uma vez e não precisa se preocupar em produzir os mesmos resultados que filtrar os dados uma vez.

O filtro deve prestar atenção à propriedade [**de \_ \_ visualização do DPS do WIA**](-wia-wiaitempropscannerdevice.md) , especialmente se algumas tarefas relacionadas ao filtro forem tratadas no hardware. Por exemplo, um determinado driver pode alterar o brilho da lâmpada no hardware do scanner, dependendo de como o aplicativo tiver definido o brilho em um item WIA 2,0. Durante a verificação final (quando o aplicativo chama [**IWiaTransfer::D aixar**](-wia-iwiatransfer-download.md)), o driver normalmente modificaria a lâmpada física do scanner. Nesse caso, o filtro de processamento de imagem pode não ter que executar nenhum processamento de brilho. Durante uma verificação de visualização, no entanto, o driver não deve modificar o brilho da lâmpada — em vez disso, isso deve ser resolvido apenas no filtro de processamento de imagem. É importante que o componente de visualização do WIA 2,0 e o filtro de processamento de imagens retornem imagens precisas com base nas propriedades definidas no item.

Um filtro de processamento de imagem deve dar suporte a todos os formatos de imagem aos quais o driver dá suporte.

O filtro de processamento de imagem sempre recebe uma imagem correspondente à área de seleção definida no item para o qual estamos adquirindo a imagem. No entanto, observe que a imagem pode ter sido girada pelo driver, caso ele dê suporte à propriedade de [**\_ \_ rotação IPS WIA**](-wia-wiaitempropscanneritem.md) .

O filtro de processamento de imagem é criado por meio de [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md), normalmente não pelo aplicativo, mas por componentes WIA 2,0 quando um aplicativo chama [**IWiaPreview:: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) ou [**IWiaTransfer::D aixar**](-wia-iwiatransfer-download.md).

A interface **IWiaImageFilter** , como todas as interfaces de Component Object Model (com), herda os métodos de interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



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



 

 
