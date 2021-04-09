---
description: Conversão automática do MTS
ms.assetid: 0848639a-26ce-47ad-8384-8969a7c3bcde
title: Conversão automática do MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d424a443995c9fff9073878a43543d4c029a2445
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089379"
---
# <a name="automatic-conversion-from-mts"></a>Conversão automática do MTS

A conversão automática ocorre em duas etapas, da seguinte maneira:

1.  Durante a instalação do Windows. A conversão é tratada pelo processo de instalação do Windows por meio do utilitário MTSTOCOM.
    > [!Note]  
    > Se a etapa 1 falhar, alguns ou todos os pacotes MTS podem, na verdade, ser convertidos, mas podem estar faltando determinadas propriedades. Nesse caso, use a ferramenta administrativa serviços de componentes para verificar todos os atributos. Os atributos do MTS ainda estarão presentes no computador (no registro do sistema em HKEY \_ computador local \_ \\ Microsoft \\ Transaction Server), mas estarão acessíveis somente por meio do utilitário regedit.exe.

     

2.  Após a última reinicialização antes da caixa de diálogo de logon do Windows ser exibida. A etapa 2 manipula as ações de conversão que exigem o acesso à rede (principalmente a criação de membros da função).
    > [!Note]  
    > Se a etapa 2 falhar (devido a falhas temporárias de rede ou controlador de domínio), será possível executar novamente o utilitário de conversão MTSTOCOM várias vezes. Para fazer isso, no prompt de comando ou depois de selecionar **executar** no menu **Iniciar** , digite o seguinte: **% windir% \\ System32 \\mtstocom.exe**.

     

## <a name="mtstocom-log-file"></a>Arquivo de log do MTSTOCOM

O utilitário MTSTOCOM gera um arquivo de log (mtstocom. log) no diretório do Windows. Esse arquivo de log mantém um registro da conversão de pacotes MTS em aplicativos COM+. Se houvesse erros durante o processo de conversão, é sempre uma boa ideia verificar o arquivo de log para obter mais informações. O arquivo de log captura problemas comuns, como usuário ou senha inválidos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Resultados e problemas de conversão de COM+](com--conversion-results-and-issues.md)
</dt> <dt>

[Conversão manual do MTS](manual-conversion-from-mts.md)
</dt> <dt>

[Biblioteca de administração MTS](mts-administration-library.md)
</dt> </dl>

 

 



