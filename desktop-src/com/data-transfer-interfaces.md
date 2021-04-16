---
title: Interfaces Transferência de Dados
description: Interfaces Transferência de Dados
ms.assetid: c42e65a4-7b77-4f39-8323-04fa60c5b140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448e1a580880c7202ec67d12965f6db7e0be99d0
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105765342"
---
# <a name="data-transfer-interfaces"></a>Interfaces Transferência de Dados

A interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) fornece aos consumidores de dados os métodos para obter e definir os dados de um objeto, determinando os formatos aos quais o objeto dá suporte e registrando e recebendo notificações quando os dados no objeto são alterados. Ao obter dados, um chamador pode especificar o formato no qual deseja renderizar os dados. A origem dos dados, no entanto, determina o meio de armazenamento, que ele retorna em um parâmetro out fornecido pelo chamador.

Por si só, o [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) fornece todas as ferramentas necessárias para implementar transferências de área de transferência do Windows ou transferências de documentos compostos em seus aplicativos. Se você também quiser dar suporte a transferências de arrastar e soltar, precisará implementar as interfaces [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) e [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) juntamente com **IDataObject**.

A interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) combinada com as APIs de área de transferência OLE fornece todos os recursos das APIs de área de transferência do Windows. Geralmente, não é necessário usar ambas as APIs da área de transferência. Os fornecedores de dados que dão suporte a transferências de arrastar e soltar ou documentos compostos OLE devem implementar a interface **IDataObject** . Se seu aplicativo der suporte apenas a transferências de área de transferência agora, mas você pretende adicionar documentos de arrastar e soltar ou compostos em versões posteriores, talvez você queira implementar o **IDataObject** e as APIs da área de transferência OLE agora para minimizar a quantidade de tempo gasto para recodificar e depurar mais tarde. Talvez você também queira implementar o **IDataObject** para utilizar a mídia de transferência que não seja a memória global.

A tabela a seguir resume quais deles usar, dependendo de quais tipos de transferência de dados você deseja oferecer suporte:



| Para dar suporte a                                                                       | Uso                                                                                                                                                                         |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Documentos compostos<br/>                                                    | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                                                                                                                               |
| Arrastar e soltar transferências<br/>                                               | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject), [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource), [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget), [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) (ou equivalente)<br/> |
| Transferências de área de transferência usando memória global exclusivamente<br/>                   | [API da área de transferência](../dataxchg/clipboard.md)<br/>                                                                                                                            |
| Transferências de área de transferência usando mídias do Exchange diferentes da memória global.<br/>  | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                                                                                                                               |
| Transferências da área de transferência agora, mas arrastar e soltar ou documentos compostos mais tarde<br/> | [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e as interfaces e funções listadas acima para "arrastar e soltar transferências"<br/>                                                    |



 

Quando um usuário inicia uma operação de transferência de dados, o aplicativo de origem cria uma instância do [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e, por meio dela, torna os dados disponíveis em um ou mais formatos. Em uma transferência de área de transferência, o aplicativo chama a função [**OleSetClipboard**](/windows/desktop/api/Ole2/nf-ole2-olesetclipboard) para passar um ponteiro de objeto de dados para OLE. (O **OleSetClipboard** também oferece formatos de dados padrão da área de transferência para aplicativos OLE versão 1 e não OLE.) Em uma transferência de arrastar e soltar, o aplicativo chama a função [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) em vez disso.

No lado de recebimento da transferência, o destino recebe o ponteiro [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) como um argumento para uma invocação de [**IDropTarget::D ROP**](/windows/desktop/api/OleIdl/nf-oleidl-idroptarget-drop) ou chamando a função [**OleSetClipboard**](/windows/desktop/api/Ole2/nf-ole2-olesetclipboard) , dependendo se a transferência é por meio de arrastar e soltar ou da área de transferência. Tendo obtido esse ponteiro, o destino chama [**IDataObject:: EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc) para saber quais formatos estão disponíveis para recuperação e em quais tipos de mídia eles podem ser obtidos. Munido dessas informações, o aplicativo de recebimento solicita os dados com uma chamada para [**IDataObject:: GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Transferência de Dados](data-transfer.md)
</dt> </dl>

 

