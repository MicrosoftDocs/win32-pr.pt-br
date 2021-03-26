---
title: Atualizar a API do Orchestrator
description: O UpdateOrchestrator agenda as atualizações automáticas de software com o impacto do usuário em mente.
ms.date: 01/14/2021
ms.topic: overview
ms.openlocfilehash: a172cccdc56d2c645bb4e7d048066ca34aea07ba
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/21/2021
ms.locfileid: "103837527"
---
# <a name="updateorchestrator-api"></a>API UpdateOrchestrator

O **UpdateOrchestrator** agenda as atualizações automáticas de software com o impacto do usuário em mente. Essa API permite que você agende o download e as instalações automáticos, juntamente com seus requisitos, para executar atualizações em um momento ideal que minimize o impacto do usuário presente. Esses recursos particularmente beneficiam os sistemas de desempenho menores com recursos de computação limitados ou mais lentos.

O Windows 19H1 inclui uma solução de primeira geração para casos de uso de atualização automática de software que foram adotados por atualizações do sistema operacional e armazenam atualizações de aplicativos e expõem uma versão inicial de ' acesso limitado ' dessa API para um conjunto selecionado de atualizadores dos aplicativos ' modo de usuário ', conforme descrito abaixo.

## <a name="features"></a>Recursos

- Registra automaticamente atualizadores de software
 
- Invoca os atualizadores de software registrados durante os tempos ideais, como durante a ausência do usuário, para atualizar ' aplicativos de modo de usuário '.
    - Inclui a capacidade de "manter acordado" em energia AC para reduzir ainda mais o impacto do usuário.

- Opera em um modelo de confiança que invoca somente atualizadores de software registrados de terceiros confiáveis
    - Há riscos substanciais ao expor UpdateOrchestrator a qualquer e a todos os chamadores, como atualizar firmware ou drivers do BIOS quando um usuário não está presente.  O UpdateOrchestrator inclui um modelo de confiança para mitigar esses riscos.

## <a name="developer-audience"></a>Público do desenvolvedor

> [!IMPORTANT]
> Atualmente, a API UpdateOrchestrator é um [recurso de acesso limitado](/uwp/api/windows.applicationmodel.limitedaccessfeatures). Essa API ficará disponível publicamente em uma versão futura.

Use a API do UpdateOrchestrator se você já tiver atualizadores de software em segundo plano para aplicativos de ' modo de usuário ' do Win32, como o atualizador da Adobe para leitor Acrobat ou de válvula. Essa interface não é necessária para aplicativos UWP/Store, pois o Microsoft Store já aproveita essa funcionalidade para atualizações de software.

Para fornecer a melhor experiência do cliente, essa versão inicial da API tem como escopo um conjunto selecionado de atualizadores registrados que atendem aos seguintes critérios:

- Atualizações somente para aplicativos de ' modo de usuário '
- Não envolva BIOS/firmware/dispositivo ou drivers de software
    - A atualização de drivers de BIOS, firmware ou dispositivo/software que não passaram por um critério de qualidade comum representa um risco substancial, especialmente quando um usuário não está presente. 
- Participar do uso dessa API envolve a capacidade de comprovar todo o conteúdo baixado e instalado por seus atualizadores de software em segundo plano nos sistemas de usuários por meio de auditorias. 

Essa API pode ser modificada significativamente antes da liberação pública.   Embora a API do UpdateOrchestrator esteja em desenvolvimento, essa versão inicial como recurso de acesso limitado é apenas para atualizadores que atendem aos critérios acima neste momento.

Nosso objetivo é melhorar a funcionalidade dessa API e reduzir o impacto de vários atualizadores de software automáticos no Windows. Agradecemos sua opinião por essa [**breve pesquisa**](https://aka.ms/UOAPISurvey) para nos ajudar a entender como a API do UpdateOrchestrator pode atender melhor às suas necessidades de desenvolvedor.

