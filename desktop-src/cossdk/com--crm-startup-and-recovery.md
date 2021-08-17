---
description: Inicialização e recuperação do COM+ CRM
ms.assetid: dee1f2df-dfe0-44c3-830b-871690e513e9
title: Inicialização e recuperação do COM+ CRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f65b8b1e32f2b587f7c288c6c5147ef30148360e89fc0a04ac952c8630076e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129188"
---
# <a name="com-crm-startup-and-recovery"></a>Inicialização e recuperação do COM+ CRM

Se um aplicativo  de servidor tiver a caixa de seleção Habilitar  gerenciadores de recursos de compensação selecionada (usando a ferramenta administrativa Serviços de Componentes, na guia Avançado da página de propriedades do aplicativo COM+), na primeira vez que ele for iniciado, ele criará um arquivo de log crm a ser usado por todos os CRMs nesse processo de aplicativo de servidor. (Para obter instruções detalhadas sobre como configurar o CRM, consulte [Configuring COM+ CRM Components](configuring-com--crm-components.md).)

O nome do arquivo de log crm criado para o aplicativo de servidor baseia-se na AppId (um GUID) do aplicativo de servidor e o arquivo de log crm é colocado no mesmo diretório que o arquivo de log do DTC (normalmente seu diretório %SystemRoot% \\ winnt \\ system32 \\ DtcLog). Os arquivos de log do CRM têm a extensão .crmlog.

> [!Note]  
> Pode ser necessário alterar o local padrão de um arquivo de log crm devido a motivos de desempenho (para ter o arquivo de log do DTC em um disco diferente do arquivo de log crm) ou talvez devido ao uso do CRM em um ambiente de cluster. O local dos arquivos de log do CRM pode ser alterado usando o SDK de administração COM+. O nome da propriedade é CRMLogFile e existe no objeto [**de coleção Applications.**](applications.md)

 

Quando um aplicativo de servidor (habilitado para CRM) é iniciado e descobre que um arquivo de log crm já existe para esse aplicativo de servidor, ele executa a recuperação nesse arquivo de log crm. *A* recuperação é o processo de concluir todas as transações que foram interrompidas por uma falha e envolve a infraestrutura de CRM que lê o arquivo de log do CRM para todas as transações que não foram totalmente concluídas. Se encontrar algum, ele contatará o DTC para determinar o resultado da transação. Em seguida, ele cria o Compensador de CRM e passa as notificações de confirmação ou anulação conforme necessário, junto com os registros de log associados.

As notificações de preparação não são recebidas pelo compensador do CRM durante a recuperação. O Compensador de CRM tem um sinalizador para distinguir se ele está sendo chamado durante a operação normal ou durante a recuperação.

Normalmente, a recuperação encontrará transações não realizadas somente se o aplicativo de servidor tiver sido desligado de forma anormal, devido a uma falha no processo de aplicativo do servidor ou a uma falha do computador. Se o aplicativo de servidor tiver permissão para desligar normalmente, devido ao tempo de ociosidade ou ao desligamento manual por meio da ferramenta administrativa serviços de componentes, o arquivo de log será limpo.

O início de um aplicativo de servidor CRM para recuperação não é iniciado automaticamente. Algumas ações externas devem ser tomadas para iniciar o aplicativo de servidor CRM em que a recuperação é necessária. Normalmente, isso seria criar um componente nesse aplicativo de servidor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos de Resource Manager COM+](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[Processo operacional do COM+ CRM](com--crm-operating-process.md)
</dt> </dl>

 

 



