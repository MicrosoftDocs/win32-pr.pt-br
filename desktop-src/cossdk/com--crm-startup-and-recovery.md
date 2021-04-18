---
description: Inicialização e recuperação do CRM do COM+
ms.assetid: dee1f2df-dfe0-44c3-830b-871690e513e9
title: Inicialização e recuperação do CRM do COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a0e631e2e5ecef1621705c9af74aa48898d733b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771289"
---
# <a name="com-crm-startup-and-recovery"></a>Inicialização e recuperação do CRM do COM+

Se um aplicativo de servidor tiver a caixa de seleção **habilitar gerenciadores de recursos de compensação** selecionada (usando a ferramenta administrativa serviços de componentes, na guia **avançado** da página de propriedades do aplicativo com+), na primeira vez que ele for iniciado, ele criará um arquivo de log do CRM a ser usado por todos os CRMS nesse processo de aplicativo do servidor. (Para obter instruções detalhadas sobre como configurar o CRM, consulte [Configurando componentes do com+ CRM](configuring-com--crm-components.md).)

O nome do arquivo de log do CRM criado para o aplicativo de servidor é baseado na AppId (um GUID) do aplicativo de servidor e o arquivo de log do CRM é colocado no mesmo diretório que o arquivo de log do DTC (normalmente seu diretório% SystemRoot% \\ WinNT \\ System32 \\ DtcLog). Os arquivos de log do CRM têm a extensão. crmlog.

> [!Note]  
> Pode ser necessário alterar o local padrão de um arquivo de log do CRM devido a motivos de desempenho (para ter o arquivo de log do DTC em um disco diferente do arquivo de log do CRM) ou talvez devido ao uso do CRM em um ambiente de cluster. O local dos arquivos de log do CRM pode ser alterado usando o SDK de administração do COM+. O nome da propriedade é CRMLogFile e existe no objeto da coleção [**Applications**](applications.md) .

 

Quando um aplicativo de servidor (que está habilitado para CRM) é iniciado e descobre que um arquivo de log do CRM já existe para esse aplicativo de servidor, ele executa a recuperação nesse arquivo de log do CRM. A *recuperação* é o processo de concluir todas as transações que foram interrompidas por uma falha e envolve a infraestrutura de CRM lendo o arquivo de log do CRM para quaisquer transações que não foram totalmente concluídas. Se ele encontrar algum, ele entrará em contato com o DTC para determinar o resultado da transação. Em seguida, ele cria o compensador de CRM e passa as notificações de confirmação ou anulação conforme necessário, junto com os registros de log associados.

As notificações de preparação não são recebidas pelo compensador de CRM durante a recuperação. O compensador de CRM tem um sinalizador para distinguir se ele está sendo chamado durante a operação normal ou durante a recuperação.

A recuperação normalmente localizará as transações não concluídas somente se o aplicativo do servidor tiver sido desligado de forma anormal, devido a uma falha de processo do aplicativo do servidor ou uma falha do computador. Se o aplicativo do servidor tiver permissão para desligar normalmente, devido ao tempo limite ocioso ou ao desligamento manual por meio da ferramenta administrativa serviços de componentes, o arquivo de log será limpo.

O início de um aplicativo do servidor CRM para recuperação não é iniciado automaticamente. Algumas ações externas devem ser executadas para iniciar o aplicativo do servidor de CRM em que a recuperação é necessária. Normalmente, isso seria criar um componente nesse aplicativo de servidor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do Gerenciador de recursos de compensação COM+](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[Processo operacional de CRM do COM+](com--crm-operating-process.md)
</dt> </dl>

 

 



