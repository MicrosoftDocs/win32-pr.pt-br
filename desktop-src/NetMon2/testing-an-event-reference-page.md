---
description: A etapa final da criação de uma página de referência de evento (ERP) é testá-la.
ms.assetid: 12690317-1cd2-496c-8a0d-ba6caca58b86
title: Testando uma página de referência de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6afaaec279403922abde578b9e73931e607680f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105779475"
---
# <a name="testing-an-event-reference-page"></a>Testando uma página de referência de evento

A etapa final da criação de uma página de referência de evento (ERP) é testá-la. Você pode testar um ERP exibindo o arquivo em um navegador HTML, como o Microsoft Internet Explorer. Ou, você pode instalar o ERP e sua DLL de especialistas para testá-lo para invocação de evento e exibi-lo no Visualizador de Eventos de Monitor de Rede.

## <a name="viewing-erps-that-have-no-dll"></a>Exibindo ERPs que não têm nenhuma DLL

Para exibir o ERP concluído sem uma DLL de especialista instalada, abra o arquivo com um visualizador de HTML que dê suporte às fontes inseridas. A ilustração a seguir mostra o exemplo de arquivo ERP descrito em [escrevendo um ERP](writing-an-event-reference-page.md) conforme ele é exibido usando o Microsoft Internet Explorer versão 4, 1.

![arquivo ERP de exemplo](images/ie-erp.png)

Testando ERPs que têm uma DLL

Depois que os arquivos ERP e a DLL de [**especialista**](experts.md) forem criados, você poderá testar a funcionalidade completa do seu ERPs com monitor de rede. Supõe-se que a DLL está depurada e possa gerar eventos válidos.

**Para testar ERPs que têm uma DLL**

1.  Verifique se a DLL de especialista correta está instalada no diretório apropriado. Para obter mais informações, consulte [instalando um especialista para Monitor de Rede 2,1](installing-an-expert-to-network-monitor-2-1.md).
2.  Verifique o [nome correto](naming-an-event-reference-page.md) do arquivo ERP.
3.  Verifique o [local correto](installing-existing-erps-to-network-monitor-2-1.md) do ERPs no diretório monitor de rede.
4.  ERPs expert de teste na interface do usuário do Monitor de Rede.
5.  Gerar um evento de teste.
6.  Verifique se o ERP aparece na Visualizador de Eventos de Monitor de Rede.

Para obter mais informações sobre como criar um ERP, consulte:

-   [Criando páginas de referência de evento expert e monitor](creating-expert-and-monitor-event-reference-pages.md)
-   [Escrevendo uma página de referência de evento](writing-an-event-reference-page.md)
-   [Nomeando uma página de referência de evento](naming-an-event-reference-page.md)

 

 



