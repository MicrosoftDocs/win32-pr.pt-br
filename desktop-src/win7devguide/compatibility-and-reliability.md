---
title: Compatibilidade e confiabilidade
description: O Windows 7 foi projetado para ser executado no mesmo hardware que o Windows Vista e ser compatível com aplicativos e drivers de dispositivo que funcionam com o Windows Vista.
ms.assetid: d7a0c335-93d1-49d3-ae40-c59ff9163f88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e9686c732c94b4b99408d0fd6e24f84079ee9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105771508"
---
# <a name="compatibility-and-reliability"></a>Compatibilidade e confiabilidade

O Windows 7 foi projetado para ser executado no mesmo hardware que o Windows Vista e ser compatível com aplicativos e drivers de dispositivo que funcionam com o Windows Vista.

O Windows 7 é a versão mais confiável do Windows ainda. Projetado em uma base tecnológica aprimorada, o Windows 7 permite que os usuários iniciem, desliguem ou hibernem seus computadores de forma confiável sem precisar se preocupar com a perda de um trabalho valioso. Além disso, o Windows 7 facilita ainda mais o backup e a restauração de dados em unidades de rede ou DVDs (discos de vídeo digital). O Windows 7 também melhora a confiabilidade e o desempenho da impressão. (Consulte [Windows 7 Application Quality Cookbook](../win7appqual/windows-7-application-quality-cookbook.md).)

## <a name="applications"></a>Aplicativos

Para ajudar a garantir a compatibilidade, o Windows 7 foi projetado em parceria estreita com fornecedores de software e fabricantes de PCs. O engajamento antecipado permitiu que a Microsoft criasse uma lista abrangente dos aplicativos mais amplamente usados. Os ciclos de testes automatizados garantem que os problemas de compatibilidade sejam detectados e corrigidos no início do ciclo de desenvolvimento. (Consulte [compatibilidade de aplicativos do Windows](/windows/apps/desktop/).)

## <a name="drivers"></a>Drivers

O Windows Driver Kit (WDK) versão 7.0.0 fornece o ambiente de compilação, as ferramentas, a documentação e os exemplos que os desenvolvedores precisam para criar drivers de qualidade para o Windows. O 7.0.0 do WDK dá suporte à análise de código-fonte estático, usando o PREfast para detectar determinadas classes de erros de codificação C e C++. O PREfast inclui um componente de driver especializado, conhecido como PFD (PREfast for drivers), que detecta erros no código de driver de modo kernel. Além disso, o WDK foi aprimorado anotando todos os arquivos de cabeçalho do kernel para obter suporte PFD. Foram adicionados novos drivers de exemplo que demonstram novas tecnologias e a documentação foi expandida.

O Windows 7 oferece suporte a uma grande variedade de produtos de software e hardware projetados para integrar perfeitamente com a plataforma. Os drivers que foram criados para o Windows Vista não devem exigir que a atualização seja executada corretamente no Windows 7. (Consulte [Kit de driver do Windows](/windows-hardware/drivers/).)

## <a name="devices"></a>Dispositivos

O Windows 7 fornece suporte flexível e robusto para uma ampla variedade de aplicativos e dispositivos, incluindo players de música, dispositivos de armazenamento, telefones celulares e outros tipos de dispositivos conectados. O teste automático desses dispositivos é usado para garantir que os problemas de compatibilidade sejam corrigidos no início do ciclo de desenvolvimento. (Consulte [conceitos básicos de classe de dispositivo do Windows](https://www.microsoft.com/whdc/device/default.mspx).)

## <a name="reliability-analysis-component"></a>Componente de análise de confiabilidade

O Componente de Análise de Confiabilidade é um agente nativo que fornece informações detalhadas da experiência do cliente com o uso e a confiabilidade do sistema. Essas informações são expostas por meio de uma interface WMI (Instrumentação de Gerenciamento do Windows) que as disponibilizam para consumo por Sistemas de Leitores Portáteis. Com a exposição do Componente de Análise de Confiabilidade por meio de uma interface WMI, os desenvolvedores podem monitorar e analisar seus aplicativos, aumentando a confiabilidade e o desempenho.

O Windows 7 usa o componente de análise de confiabilidade interno para calcular um índice de confiabilidade que fornece informações sobre o uso geral do sistema e a estabilidade ao longo do tempo. O Componente de Análise de Confiabilidade também acompanha todas as alterações importantes do sistema que podem ter um impacto sobre a estabilidade, como atualizações do Windows e instalações de aplicativos. Você pode usar o snap-in do monitor de confiabilidade para ver as tendências no índice de confiabilidade do sistema correlacionados a esses eventos potencialmente de desestabilização, facilitando o rastreamento de uma alteração de confiabilidade diretamente em um evento específico. (Consulte a [função MountVHD](/previous-versions/windows/desktop/msvs/mountvhd).)

 

 