---
description: Antes do Windows Vista, você criou um item do painel de controle criando um arquivo. dll e nomeando-o com uma extensão. cpl.
ms.assetid: 258dae28-c054-4392-b0e9-99493f23c814
title: Usando CPLApplet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1e59b29dd7c082822ed63d425dd4967a542b5d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967882"
---
# <a name="using-cplapplet"></a>Usando CPLApplet

Antes do Windows Vista, você criou um item do painel de controle criando um arquivo. dll e nomeando-o com uma extensão. cpl. Esse arquivo exportou a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) . Esse esquema ainda tem suporte no Windows Vista e em versões posteriores e é discutido neste tópico. No entanto, as diretrizes para novos itens do painel de controle recomendam uma abordagem mais simples com o item do painel de controle criado como um arquivo. exe que usa um layout de fluxo de tarefas.

Quando o painel de controle carrega um arquivo. dll (ou. cpl), ele chama a função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) para obter informações como o número de itens do painel de controle que o arquivo hospeda, bem como informações sobre cada item. O painel de controle também chama a função quando a janela do item é inicializada, aberta ou fechada.

Quando o Windows carrega o item do painel de controle pela primeira vez, ele recupera o endereço da função [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) e, subsequentemente, usa esse endereço para chamar a função e passá-la para as mensagens. Ele pode enviar as seguintes mensagens.



| Mensagem                                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CPL \_ DBLCLK**](cpl-dblclk.md)           | Enviado para notificar [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) que o usuário escolheu o ícone associado a um determinado item do painel de controle. **CPlApplet** deve exibir a caixa de diálogo para o item especificado e executar qualquer tarefa especificada pelo usuário. O parâmetro **CPlApplet** *lParam1* é um inteiro que representa o índice de base zero do item do painel de controle. O parâmetro *lParam2* é o ponteiro **lpData** retornado na estrutura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) ou [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) na mensagem [**CPL \_ inquire**](cpl-inquire.md) ou [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) . O valor de retorno é ignorado.                                                                |
| [**CPL de \_ saída**](cpl-exit.md)               | Enviado após a última mensagem de parada de CPL \_ e imediatamente antes de o Windows usar a função [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) para liberar a DLL que contém o item do painel de controle. O [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) deve liberar qualquer memória restante e se preparar para fechar. O valor de retorno é ignorado.                                                                                                                                                                                                                                                                                                                                                                                                |
| [**CPL \_ GETcount**](cpl-getcount.md)       | Enviado após a mensagem de inicialização de CPL \_ para solicitar [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) para retornar um número que indica quantos subprogramas ele oferece suporte.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**CPL \_ init**](cpl-init.md)               | Enviado imediatamente depois que a DLL que contém o item do painel de controle é carregada. A mensagem solicita que o [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) execute procedimentos de inicialização, incluindo a alocação de memória.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**CPL de \_ consulta**](cpl-inquire.md)         | Enviado após a \_ mensagem de sqlcount do CPL para solicitar [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) para fornecer informações sobre um subprograma especificado. O valor de *lParam1* é um inteiro que representa o índice de base zero do subprograma sobre o qual as informações estão sendo solicitadas. O parâmetro *lParam2* de **CPlApplet** aponta para uma estrutura [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) . O valor de retorno é ignorado.                                                                                                                                                                                                                                                                                                    |
| [**CPL \_ NEWINQUIRE**](cpl-newinquire.md)   | Enviado após a \_ mensagem de sqlcount do CPL para solicitar [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) para fornecer informações sobre um item do painel de controle especificado. O valor de *lParam1* é um inteiro que representa o índice de base zero do subprograma sobre o qual as informações estão sendo solicitadas. O parâmetro *lParam2* é um ponteiro para uma estrutura [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) . CPL \_ NEWINQUIRE normalmente deve ser ignorado. Seu aplicativo deve processar somente a \_ consulta CPL no windows 95, no Microsoft Windows NT 4,0 e em sistemas posteriores, pois o desempenho do painel de controle sofre quando o CPL \_ NEWINQUIRE é usado. Isso ocorre porque as cadeias de caracteres e os ícones retornados não podem ser armazenados em cache. O valor de retorno é ignorado. |
| [**CPL de \_ seleção**](cpl-select.md)           | Obsoleto. As versões atuais do Windows não enviam essa mensagem.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**CPL \_ STARTWPARMS**](cpl-startwparms.md) | Enviado para notificar [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) que o usuário escolheu o ícone associado a uma determinada caixa de diálogo. **CPlApplet** deve exibir a caixa de diálogo correspondente e executar qualquer tarefa especificada pelo usuário. Essa mensagem é semelhante a CPL \_ DBLCLK, mas pode haver algumas informações adicionais. O parâmetro *lParam1* é o número de item do painel de controle e *LParam2* é um **LPCTSTR** para qualquer direção extra que possa ser necessária. Retornar **true** se esta mensagem for tratada; caso contrário, **false**. Esta mensagem é válida para a [versão 5, 0](versions.md) e posterior do Shell32.dll.                                                                                         |
| [**CPL de \_ parada**](cpl-stop.md)               | Enviado uma vez para cada item do painel de controle no arquivo. cpl antes que o Windows descarregue a extensão do painel de controle. [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) deve liberar qualquer memória associada ao número de item fornecido em *lParam1*. O parâmetro *lParam2* é um ponteiro **lpData** retornado na [**estrutura CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) ou [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) na mensagem [**CPL \_ inquire**](cpl-inquire.md) ou [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) . O valor de retorno é ignorado.                                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Itens do painel de controle](control-panel-applications.md)
</dt> <dt>

[Diretrizes da Experiência do Usuário](user-experience-guidelines.md)
</dt> <dt>

[Registrando itens do painel de controle](registering-control-panel-items.md)
</dt> <dt>

[Processamento de mensagens do painel de controle](message-processing.md)
</dt> <dt>

[Executando itens do painel de controle](executing-control-panel-items.md)
</dt> <dt>

[Estendendo itens do painel de controle do sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Atribuindo categorias do painel de controle](assigning-control-panel-categories.md)
</dt> <dt>

[Criando links de tarefas pesquisáveis para um item do painel de controle](creating-searchable-task-links.md)
</dt> <dt>

[Acessando o painel de controle no modo de segurança no Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 
