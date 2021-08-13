---
description: Conversão automática do MTS
ms.assetid: 0848639a-26ce-47ad-8384-8969a7c3bcde
title: Conversão automática do MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e02cc3889c479d829290b22b71edf13cc4ebc8f419c333d5e99390d47c01da65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549483"
---
# <a name="automatic-conversion-from-mts"></a>Conversão automática do MTS

A conversão automática ocorre em duas etapas, da seguinte forma:

1.  Durante Windows configuração. A conversão é manipulada pelo processo Windows configuração por meio do utilitário MTSTOCOM.
    > [!Note]  
    > Se a etapa 1 falhar, alguns ou todos os pacotes MTS poderão realmente ter sido convertidos, mas poderão não ter determinadas propriedades. Nesse caso, use a ferramenta administrativa Serviços de Componentes para verificar todos os atributos. Os atributos do MTS ainda estarão presentes no computador (no registro do sistema em HKEY LOCAL MACHINE Microsoft Transaction Server), mas só estarão acessíveis por meio do utilitário \_ \_ \\ \\ regedit.exe.

     

2.  Após a última reinicialização antes da Windows caixa de diálogo de logon do banco de dados é exibida. A Etapa 2 lida com as ações de conversão que exigem acesso à rede (principalmente criação de membro de função).
    > [!Note]  
    > Se a etapa 2 falhar (devido a falhas temporárias de rede ou controlador de domínio), será possível realizar a rerun do utilitário de conversão MTSTOCOM qualquer número de vezes. Para fazer isso, no prompt  de comando ou depois de selecionar Executar no **menu** Iniciar, digite o seguinte: **%windir% \\ system32 \\mtstocom.exe**.

     

## <a name="mtstocom-log-file"></a>Arquivo de log MTSTOCOM

O utilitário MTSTOCOM gera um arquivo de log (Mtstocom.log) no diretório Windows. Esse arquivo de log mantém um registro da conversão de pacotes MTS em aplicativos COM+. Se houver erros durante o processo de conversão, é sempre uma boa ideia verificar o arquivo de log para obter mais informações. O arquivo de log captura problemas comuns, como usuário inválido ou senha.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resultados e problemas de conversão COM+](com--conversion-results-and-issues.md)
</dt> <dt>

[Conversão manual do MTS](manual-conversion-from-mts.md)
</dt> <dt>

[Biblioteca de Administração do MTS](mts-administration-library.md)
</dt> </dl>

 

 



