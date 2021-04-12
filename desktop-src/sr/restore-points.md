---
title: Pontos de restauração
description: Os pontos de restauração são criados para permitir que os usuários escolham os Estados anteriores do sistema. Cada ponto de restauração contém as informações necessárias para restaurar o sistema para o estado escolhido. Os pontos de restauração são criados antes que as principais alterações sejam feitas no sistema.
ms.assetid: 5f68b377-4293-493e-afaf-f4414c2af1fb
author: Teresa-Motiv
ms.author: v-tea
ms.topic: article
ms.date: 12/06/2019
manager: dcscontentpm
ms.custom: CSSTroubleshooting
ms.openlocfilehash: 6ef1aba7d1cb018bb3fa4f32d868828ef2ac4d1b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294379"
---
# <a name="restore-points"></a>Pontos de restauração

Os pontos de restauração são criados para permitir que os usuários selecionem um estado de sistema anterior. Cada ponto de restauração contém as informações necessárias para restaurar o sistema para o estado selecionado. Os pontos de restauração são criados antes que as principais alterações sejam feitas no sistema.

A restauração do sistema gerencia automaticamente o espaço em disco que é alocado para pontos de restauração. Ele limpa os pontos de restauração mais antigos para liberar espaço para os novos. A restauração do sistema aloca espaço com base no tamanho do disco rígido e na versão do Windows que o computador executa, conforme mostrado na tabela a seguir.

|Versão do Windows |&nbsp;Tamanho do disco rígido |Espaço de restauração do sistema |
| --- | --- | --- |
|Windows 7 e versões posteriores | > 64 GB |Até cinco% do espaço total em disco ou um máximo de 10 GB, o que for menor |
|  | &le; 64 GB |Até três por cento do espaço total em disco |
|Windows Vista |  |Até 15% do espaço total em disco ou um máximo de 30% do espaço em disco disponível, o que for menor |
|Windows XP | >4 GB |Até 12% do espaço total em disco<br /><br />Para alterar o limite máximo de armazenamento no Windows XP, use o item **sistema** no painel de controle. |
|  | \< 4 GB |Até 400 MB |

## <a name="event-triggered-restore-points"></a>Pontos de restauração disparados por evento

A restauração do sistema cria automaticamente um ponto de restauração antes que qualquer um dos seguintes eventos ocorra:

- **Instalação do aplicativo** (aplica-se somente a aplicativos que usam um instalador em conformidade com a restauração do sistema). Se a instalação do aplicativo causar problemas no sistema, o usuário poderá restaurar o sistema para um estado que preceda a instalação.
- **Instalação do Windows Update ou do AutoUpdate**. Windows Update (anteriormente conhecido como atualização automática) baixa e instala automaticamente as atualizações do Windows. Além disso, ele fornece uma maneira fácil para os usuários baixarem e instalarem atualizações manualmente. A restauração do sistema cria um ponto de restauração antes que uma atualização seja instalada, seja automaticamente ou manual.
- **Operação de restauração do sistema**. A restauração do sistema cria automaticamente um ponto de restauração como um backup antes de qualquer operação de restauração ser iniciada. Por exemplo, suponha que um usuário rearmazene acidentalmente o Windows em um ponto de restauração incorreto. Para desfazer essa restauração, o usuário pode restaurar o Windows para um ponto de restauração anterior ao primeiro ponto de restauração. Depois que o Windows tiver sido restaurado para seu estado inicial, o usuário poderá repetir o processo, desta vez selecionando o ponto de restauração correto.

## <a name="scheduled-restore-points"></a>Pontos de restauração agendados

Os usuários podem configurar a restauração do sistema para criar pontos de restauração em intervalos regulares. Os usuários também podem criar e nomear manualmente um ponto de restauração a qualquer momento de dentro da interface do usuário de restauração do sistema. Esses pontos de restauração são salvos e compactados e estão disponíveis na lista de pontos de restauração.

No Windows 7 e versões posteriores, a restauração do sistema criará um ponto de restauração agendado somente se nenhum outro ponto de restauração tiver sido criado nos sete dias anteriores. No Windows Vista, a restauração do sistema cria um ponto de verificação a cada 24 horas se nenhum outro ponto de restauração foi criado naquele dia. No Windows XP, a restauração do sistema cria um ponto de verificação a cada 24 horas, independentemente de outras operações.

## <a name="known-issue-you-cannot-restore-the-system-to-a-restore-point-after-you-install-a-windows-10-update"></a>Problema conhecido: não é possível restaurar o sistema para um ponto de restauração depois de instalar uma atualização do Windows 10

Considere o cenário a seguir.

1. Você instala o Windows 10 em um computador limpo.
1. Você ativa a proteção do sistema e, em seguida, cria um ponto de restauração do sistema chamado "R1".
1. Você instala uma ou mais atualizações do Windows 10.
1. Depois que as atualizações terminarem de ser instaladas, você restaurará o sistema para o ponto de restauração "R1".

Nesse cenário, o sistema não é restaurado para o ponto de restauração "R1". Em vez disso, o computador passa por um erro de parada (0xC000021A). Você reinicia o computador, mas o sistema não pode retornar à área de trabalho do Windows.

### <a name="cause"></a>Causa

Esse é um problema conhecido no Windows 10.

Durante o processo de restauração do sistema, o Windows prepara temporariamente a restauração de arquivos que estão em uso. Em seguida, ele salva as informações no registro. Quando o computador é reiniciado, ele conclui a operação em etapas.

Nessa situação, o Windows restaura os arquivos de catálogo e prepara os arquivos de driver (. sys) a serem restaurados quando o computador é reiniciado. No entanto, quando o computador é reiniciado, o Windows carrega os drivers existentes antes de restaurar as versões posteriores dos drivers. Como as versões do driver não correspondem às versões dos arquivos de catálogo restaurados, o processo de reinicialização é interrompido.

### <a name="workaround"></a>Solução alternativa

**Para se recuperar da reinicialização com falha e continuar o processo de restauração**

Depois que a falha ocorrer, reinicie o computador até ele entrar no ambiente de recuperação do Windows (WinRE). Para fazer isso, talvez seja necessário usar uma opção de reinicialização de hardware, e talvez seja necessário reiniciar várias vezes.

No ambiente de recuperação do Windows:

1. Selecione **solução de problemas**  >  **Opções avançadas**  >  **mais opções de recuperação**  >  **configurações de inicialização** e, em seguida, selecione **reiniciar agora**.
1. Na lista de configurações de inicialização, selecione **desabilitar imposição de assinatura de driver**.
   > [!NOTE]  
   > Talvez seja necessário usar a tecla F7 para selecionar essa configuração.
1. Deixe o processo de inicialização continuar. Quando o Windows é reiniciado, o processo de restauração do sistema deve ser retomado e concluído.

Essas etapas restauram o computador para o estado "R1".

**Para se recuperar da reinicialização com falha**

Para se recuperar da reinicialização com falha e reverter o processo de restauração, siga estas etapas:

1. Conforme descrito no procedimento anterior, reinicie o computador e, em seguida, digite WinRE.  
1. No ambiente de recuperação do Windows, selecione **solucionar problemas**  >  de **Opções avançadas**  >  **restauração do sistema** e, em seguida, selecione **desfazer restauração do sistema**.

Essas etapas retornam o computador para o estado em que estava antes de você iniciar o processo de restauração.

**Para restaurar o Windows para um ponto de restauração usando o WinRE**

Para iniciar o assistente de restauração do sistema em um computador afetado, use WinRE em vez da caixa de diálogo **configurações** . Para fazer isso, siga estas etapas:

1. Selecione **Iniciar**  >  **configurações**  >  **Atualizar & segurança**  >  **recuperação**.
1. Em **Opções avançadas**, selecione **reiniciar agora**.
1. Depois que o WinRE for iniciado, selecione **solucionar problemas** de  >  **Opções avançadas**  >  **restauração do sistema**.
1. Insira sua chave de recuperação, pois ela é mostrada na tela e siga as instruções no assistente de restauração do sistema.

### <a name="references"></a>Referências

Para obter mais informações sobre como usar o WinRE, consulte os seguintes artigos:

- [Ambiente de recuperação do Windows (Windows RE)](/windows-hardware/manufacture/desktop/windows-recovery-environment--windows-re--technical-reference)
- [Inicie seu PC no modo de segurança no Windows 10](https://support.microsoft.com/help/12376) 