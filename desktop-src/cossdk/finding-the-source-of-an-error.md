---
description: Localizando a origem de um erro
ms.assetid: d7287cf1-9501-4d37-b022-b56c8008220c
title: Localizando a origem de um erro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b505981f12a6f8b23adc22e92cfc7b7c4b77b7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010263"
---
# <a name="finding-the-source-of-an-error"></a>Localizando a origem de um erro

Você pode diagnosticar a origem e obter uma descrição dos erros do aplicativo usando COM+ e outras ferramentas. Se você descobrir que o erro do aplicativo é causado por COM+, poderá interpretar a mensagem de erro exibindo o arquivo Winerror. h ou usando o utilitário de erro Microsoft Visual C++.

Se o aplicativo do servidor estiver falhando ou causando um comportamento inesperado, primeiro você deverá determinar onde ocorreu o erro. O sistema Visualizador de Eventos rastreia eventos de aplicativo, segurança e sistema. Muitos erros "silenciosos" são registrados aqui. No entanto, nem todos os erros são mostrados no Visualizador de Eventos.

Primeiro, você deve consultar o log do aplicativo no Visualizador de Eventos para verificar o aplicativo associado à mensagem do evento. (Como você também pode arquivar logs de eventos, é possível acompanhar um histórico de eventos do erro.) Clicar duas vezes em uma entrada no log ativa uma página de **Propriedades do evento** , que fornece mais informações sobre o evento do sistema.

Para obter mais informações sobre como depurar um aplicativo COM+, consulte [Depurando aplicativos com+](debugging-com--applications.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Política de FailFast e isolamento de falhas](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Como o COM+ modifica valores de retorno](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretando códigos de erro](interpreting-error-codes.md)
</dt> <dt>

[Estratégias para lidar com erros no COM+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Solução de problemas](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



