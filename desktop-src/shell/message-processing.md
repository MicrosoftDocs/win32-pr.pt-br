---
description: A função de retorno de chamada CPlApplet processa todas as mensagens enviadas a um item do painel de controle por Windows. As mensagens enviadas para a função estão em uma ordem específica. Pelo mesmo token, o item de .cpl requer que as mensagens sejam processadas de uma maneira específica.
ms.assetid: 70302698-f9d5-4de4-a662-4815002eea52
title: Processamento de mensagens do painel de controle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e697c603b69790d17c4d6771666a1111fa6f968eb97a30256696921f133530d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719947"
---
# <a name="control-panel-message-processing"></a>Processamento de mensagens do painel de controle

A função de retorno de chamada [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) processa todas as mensagens enviadas a um item do painel de controle por Windows. As mensagens enviadas para a função estão em uma ordem específica. Pelo mesmo token, o item de .cpl requer que as mensagens sejam processadas de uma maneira específica.

primeiro, a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) recebe a \_ mensagem CPL INIT quando Windows primeiro carrega o item do painel de controle. A função deve executar qualquer inicialização, como alocar memória e retornar diferente de zero. se **CPlApplet** não puder concluir a inicialização, ela deverá retornar zero, direcionando Windows para encerrar a comunicação e liberar a DLL.

em seguida, se a mensagem de inicialização de cpl tiver sido \_ bem-sucedida, Windows enviará a \_ mensagem cpl getcount. A função deve retornar o número de itens do painel de controle com suporte pelo arquivo .dll.

A função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) recebe uma mensagem CPL \_ inquire e uma \_ mensagem CPL NEWINQUIRE para cada item do painel de controle com suporte no arquivo .dll. A função preenche uma estrutura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) ou [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) com informações sobre o item, como seu nome, ícone e uma cadeia de caracteres descritiva. A maioria dos aplicativos deve processar a \_ mensagem de consulta cpl e ignorar a \_ mensagem CPL NEWINQUIRE. a \_ mensagem CPL inquire fornece informações em um formato que Windows pode armazenar em cache, o que resulta em um desempenho muito melhor. A \_ mensagem CPL NEWINQUIRE será usada somente se você precisar alterar o ícone do item ou exibir cadeias de caracteres com base no estado do computador. os itens do painel de controle que usam CPL \_ NEWINQUIRE não podem ser encontrados por uma pesquisa de menu **iniciar** no Windows Vista porque ele depende do cache.

A função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) em seguida recebe uma \_ mensagem CPL DBLCLK como uma notificação de que o usuário escolheu o ícone que representa o item do painel de controle. A função pode receber essa mensagem várias vezes. A mensagem inclui o identificador de item e o ponteiro **lpData** retornado na estrutura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) ou [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) na chamada para [**CPL \_ inquire**](cpl-inquire.md) ou [**CPL \_ NEWINQUIRE**](cpl-newinquire.md). A função deve exibir a caixa de diálogo correspondente e processar a entrada do usuário subsequente.

Além de CPL \_ DBLCLK, a \_ mensagem CPL STARTWPARMS pode ser enviada se um item do painel de controle for invocado com parâmetros de entrada, como de um prompt de comando ou de outro programa. A mensagem inclui o identificador de item junto com a cadeia de caracteres de parâmetro adicional.

Antes de o aplicativo de controle ser encerrado, o [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) recebe a mensagem de parada de CPL \_ uma vez para cada item do painel de controle com suporte pelo arquivo de .dll. A mensagem inclui o identificador para o item do painel de controle e o ponteiro **lpData** retornado na estrutura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) ou [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) na chamada para [**CPL \_ inquire**](cpl-inquire.md) ou [**CPL \_ NEWINQUIRE**](cpl-newinquire.md). A função deve liberar qualquer memória alocada para a caixa de diálogo especificada.

Após a última mensagem de parada de CPL \_ , [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) recebe uma mensagem de saída de CPL \_ . A função deve liberar toda a memória alocada restante e cancelar o registro de qualquer classe de janela privada que ela possa ter registrado. imediatamente após a função retornar dessa mensagem, Windows libera o item do painel de controle chamando a função [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Itens do painel de controle](control-panel-applications.md)
</dt> <dt>

[Diretrizes da Experiência do Usuário](user-experience-guidelines.md)
</dt> <dt>

[Registrando itens do painel de controle](registering-control-panel-items.md)
</dt> <dt>

[Usando CPLApplet](using-cplapplet.md)
</dt> <dt>

[Executando itens do painel de controle](executing-control-panel-items.md)
</dt> <dt>

[Estendendo itens do painel de controle do sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Atribuindo categorias do painel de controle](assigning-control-panel-categories.md)
</dt> <dt>

[Criando links de tarefas pesquisáveis para um item do painel de controle](creating-searchable-task-links.md)
</dt> <dt>

[acessando o painel de controle no modo de Cofre em Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
