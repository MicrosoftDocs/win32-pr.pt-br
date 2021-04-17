---
title: Notificação de dados
description: Os objetos que consomem dados de uma fonte externa às vezes precisam ser informados quando os dados nessa fonte são alterados.
ms.assetid: 286a1ecf-5255-4443-a17d-5ffa55ed0be1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49df9e6bb7d9b15192473b18114fe7fcd69ecedf
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105811577"
---
# <a name="data-notification"></a>Notificação de dados

Os objetos que consomem dados de uma fonte externa às vezes precisam ser informados quando os dados nessa fonte são alterados. Por exemplo, um visualizador de fita com cotação de ações que depende de dados em algumas planilhas precisa ser notificado quando esses dados são alterados para que ele possa atualizar sua exibição. Da mesma forma, um documento composto precisa de informações sobre as alterações de dados em seus objetos incorporados para que ele possa atualizar seus caches de dados. Em casos como esse, em que a atualização dinâmica de dados é desejável, as fontes de dados exigem algum mecanismo de notificação de consumidores de dados de alterações à medida que ocorrem sem OBLIGATING os consumidores a descartar tudo para atualizar seus dados. De preferência, ter sido notificado de que ocorreu uma alteração na fonte de dados, um objeto de consumo pode solicitar uma cópia atualizada em seu lazer.

O mecanismo de COM para lidar COM notificações assíncronas desse tipo é um objeto chamado de coletor de aviso, que é simplesmente qualquer objeto COM que implementa uma interface chamada [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink). Os consumidores de dados implementam o **IAdviseSink**. Eles se registram para receber notificações ao entregar um ponteiro para o objeto de dados de interesse.

As interfaces [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) expõe os seguintes métodos para receber notificações assíncronas:



| Método                                                      | Notifica o coletor de aviso que                                            |
|-------------------------------------------------------------|--------------------------------------------------------------------------|
| [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange)<br/> | Os dados do objeto de chamada foram alterados.<br/>                        |
| [**OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange)<br/> | As instruções para desenhar o objeto de chamada foram alteradas.<br/> |
| [**Renomear**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onrename)<br/>         | O moniker do objeto de chamada foi alterado.<br/>                     |
| [**OnSave**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onsave)<br/>             | O objeto de chamada foi salvo no armazenamento persistente.<br/>      |
| [**Fechamento**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onclose)<br/>           | O objeto de chamada foi fechado.<br/>                           |



 

Como a tabela indica, a interface [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) expõe métodos para notificar o coletor de avisos de eventos diferentes das alterações nos dados do objeto de chamada. O objeto de chamada também pode notificar o coletor quando o modo no qual ele se desenha altera, ou é renomeado, salvo ou fechado. Essas outras notificações são usadas principalmente ou inteiramente no contexto de documentos compostos, embora o mecanismo de notificação seja idêntico. Para obter mais informações sobre notificações de documentos compostos, consulte "documentos compostos".

Para aproveitar o coletor de avisos, uma fonte de dados deve implementar [**IDataObject::D Advise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-dadvise), [**IDataObject::D Unadvise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-dunadvise)e [**IDataObject:: EnumDAdvise**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-enumdadvise). Um consumidor de dados chama o **DAdvise** mothod para notificar um objeto de dados de que ele deseja ser notificado quando os dados do objeto forem alterados. O objeto de consumo chama o método **DUnadvise** para desmontar essa conexão. Qualquer parte interessada pode chamar o método **EnumDAdvise** para saber o número de objetos que têm uma conexão de consultoria com um objeto de dados.

Quando os dados são alterados na origem, o objeto de dados chama [**IAdviseSink:: OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange) em todos os consumidores de dados que se registraram para receber notificações. Para controlar as conexões de consultoria e gerenciar a expedição de notificações, as fontes de dados dependem de um objeto chamado de um *detentor de aviso de dados*. Você pode criar seu próprio detentor de aviso de dados implementando a interface [**IDataAdviseHolder**](/windows/desktop/api/ObjIdl/nn-objidl-idataadviseholder) . Ou, você pode deixar COM que o COM faça isso chamando a função auxiliar [**CreateDataAdviseHolder**](/windows/win32/api/ole2/nf-ole2-createdataadviseholder).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Transferência de Dados](data-transfer.md)
</dt> </dl>

 

