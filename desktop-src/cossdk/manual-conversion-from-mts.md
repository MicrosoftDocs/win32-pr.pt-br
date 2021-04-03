---
description: Conversão manual do MTS
ms.assetid: 7ecc64a8-783d-4238-8b63-8e9c76382723
title: Conversão manual do MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e5fab25721738d497c943a166f899c73927b13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646349"
---
# <a name="manual-conversion-from-mts"></a>Conversão manual do MTS

Talvez você queira isolar a conversão de pacotes MTS em aplicativos COM+ para que ele esteja fora do processo de instalação do Windows. O procedimento a seguir oferece uma abordagem alternativa:

1.  Exporte os pacotes MTS usando o recurso de exportação de pacote MTS 2,0 (resultando em um arquivo de pacote MTS e uma coleção de outros arquivos).
2.  Exclua os pacotes MTS e atualize o Windows ou execute uma instalação limpa do Windows.
3.  Instale os arquivos de pacote MTS (. Pak) em um sistema Windows 2000 ou posterior usando o assistente de instalação de aplicativo da ferramenta administrativa serviços de componentes. Também será necessário redefinir a identidade "executar como" do aplicativo no registro do sistema em **HKEY \_ local \_ Machine \\ software \\ classes \\ AppID \\ runas**.

> [!Note]  
> Somente o procedimento de conversão automática (por meio da instalação do Windows ou executando o utilitário MTSTOCOM) gera o arquivo de log MTSTOCOM. Esse arquivo não é gerado ao seguir o procedimento de conversão manual.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conversão automática do MTS](automatic-conversion-from-mts.md)
</dt> <dt>

[Resultados e problemas de conversão de COM+](com--conversion-results-and-issues.md)
</dt> <dt>

[Biblioteca de administração MTS](mts-administration-library.md)
</dt> </dl>

 

 



