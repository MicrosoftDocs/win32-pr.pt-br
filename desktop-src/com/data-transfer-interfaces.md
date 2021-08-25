---
title: Interfaces de transferência de dados
description: Interfaces de transferência de dados
ms.assetid: c42e65a4-7b77-4f39-8323-04fa60c5b140
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63bffa72f2e6bd408cbb7f19121aeef991e74702ff1141b24aba779e6985585c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896336"
---
# <a name="data-transfer-interfaces"></a>Interfaces de transferência de dados

A interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) fornece aos consumidores de dados métodos para obter e definir os dados de um objeto, determinando quais formatos o objeto dá suporte e registrando e recebendo notificações quando os dados no objeto são atualizados. Ao obter dados, um chamador pode especificar o formato no qual deseja renderizar os dados. A origem dos dados, no entanto, determina a mídia de armazenamento, que ela retorna em um parâmetro out fornecido pelo chamador.

Por si só, [**o IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) fornece todas as ferramentas necessárias para implementar Windows transferências de área de transferência ou transferências de documentos compostas em seus aplicativos. Se você também quiser dar suporte a transferências de arrastar e soltar, precisará implementar as interfaces [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) e [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) juntamente com **IDataObject**.

A interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) combinada com APIs de área de transferência OLE fornece todos os recursos das APIs Windows área de transferência. Geralmente, não é necessário usar ambas as APIs da área de transferência. Os fornecedores de dados que suportam transferências de arrastar e soltar ou documentos compostos OLE devem implementar a interface **IDataObject.** Se o aplicativo dá suporte apenas a transferências de área de transferência agora, mas você pretende adicionar documentos arrastar e soltar ou compostos em versões posteriores, talvez você queira implementar **IDataObject** e as APIs da área de transferência OLE agora para minimizar a quantidade de tempo gasto para recodificar e depurar posteriormente. Talvez você também queira implementar **IDataObject** para utilizar a mídia de transferência que não seja a memória global.

A tabela a seguir resume quais usar, dependendo de quais tipos de transferência de dados você deseja dar suporte:



| Para dar suporte                                                                       | Usar                                                                                                                                                                         |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Documentos compostos<br/>                                                    | [**Idataobject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                                                                                                                               |
| Arrastar e soltar transferências<br/>                                               | [**IDataObject,**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) [**IDropSource,**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) [**IDropTarget,**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) (ou o equivalente)<br/> |
| Transferências da área de transferência usando a memória global exclusivamente<br/>                   | [API da área de transferência](../dataxchg/clipboard.md)<br/>                                                                                                                            |
| Transferências de área de transferência usando mídias de troca que não a memória global.<br/>  | [**Idataobject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject)<br/>                                                                                                                               |
| Transferências da área de transferência agora, mas arrastar e soltar ou documentos compostos mais tarde<br/> | [**IDataObject e**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) as interfaces e a função listadas acima para "Arrastar e soltar transferências"<br/>                                                    |



 

Quando um usuário inicia uma operação de transferência de dados, o aplicativo de origem cria uma instância [**de IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e, por meio dela, disponibiliza os dados em um ou mais formatos. Em uma transferência de área de transferência, o aplicativo chama a [**função OleSetClipboard**](/windows/desktop/api/Ole2/nf-ole2-olesetclipboard) para passar um ponteiro de objeto de dados para OLE. (**O OleSetClipboard** também oferece formatos de dados de área de transferência padrão para aplicativos OLE versão 1 e não OLE.) Em uma transferência de arrastar e soltar, o aplicativo chama a [**função DoDragDrop.**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)

No lado de recebimento da transferência, o destino recebe o ponteiro [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) como um argumento para uma invocação de [**IDropTarget::D rop**](/windows/desktop/api/OleIdl/nf-oleidl-idroptarget-drop) ou chamando a [**função OleSetClipboard,**](/windows/desktop/api/Ole2/nf-ole2-olesetclipboard) dependendo se a transferência é por meio de arrastar e soltar ou da área de transferência. Depois de obter esse ponteiro, o destino chama [**IDataObject::EnumFormatEtc**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumformatetc) para saber quais formatos estão disponíveis para recuperação e em quais tipos de mídia eles podem ser obtidos. Com essas informações, o aplicativo receptor solicita os dados com uma chamada para [**IDataObject::GetData.**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Transferência de dados](data-transfer.md)
</dt> </dl>

 

