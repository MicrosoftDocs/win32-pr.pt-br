---
title: Compatibilidade e confiabilidade
description: Windows 7 foi projetado para ser executado no mesmo hardware que o Windows Vista e ser compatível com aplicativos e drivers de dispositivo que funcionam com o Windows Vista.
ms.assetid: d7a0c335-93d1-49d3-ae40-c59ff9163f88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e42dbf564fc524fbfb620746cea84e387fbe9f76484ce9e0d87803f55dae4b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119706296"
---
# <a name="compatibility-and-reliability"></a>Compatibilidade e confiabilidade

Windows 7 foi projetado para ser executado no mesmo hardware que o Windows Vista e ser compatível com aplicativos e drivers de dispositivo que funcionam com o Windows Vista.

Windows 7 é a versão mais confiável do Windows ainda. Projetado em uma base de tecnologia aprimorada, o Windows 7 permite que os usuários iniciem, desliguem ou hibernam seus computadores de forma confiável sem precisar se preocupar com a perda de trabalho valioso. Além disso, Windows 7 torna mais fácil do que nunca fazer backup e restaurar dados em unidades de rede ou DVDs (discos de vídeo digital). Windows 7 também melhora a confiabilidade e o desempenho da impressão. (Consulte [Windows 7 Application Quality Cookbook](../win7appqual/windows-7-application-quality-cookbook.md).)

## <a name="applications"></a>Aplicativos

Para ajudar a garantir a compatibilidade, Windows 7 foi projetado em parceria estreita com fornecedores de software e fabricantes de COMPUTADORES. O envolvimento antecipado permitiu que a Microsoft cria uma lista abrangente dos aplicativos mais amplamente usados. Ciclos de teste automatizados garantem que os problemas de compatibilidade sejam detectados e corrigidos no início do ciclo de desenvolvimento. (Consulte [Windows Compatibilidade do aplicativo](/windows/apps/desktop/).)

## <a name="drivers"></a>Drivers

O WDK (Kit de Driver do Windows) versão 7.0.0 fornece o ambiente de build, as ferramentas, a documentação e os exemplos que os desenvolvedores precisam para criar drivers de qualidade para Windows. O WDK 7.0.0 dá suporte à análise de código-fonte estático, usando PREfast para detectar determinadas classes de erros de codificação C e C++. O PREfast inclui um componente de driver especializado, conhecido como PREfast para drivers (PFD), que detecta erros no código do driver no modo kernel. Além disso, o WDK foi aprimorado anotando todos os arquivos de título do kernel para suporte a PFD. Novos drivers de exemplo foram adicionados que demonstram novas tecnologias e a documentação foi expandida.

Windows 7 dá suporte a uma grande variedade de produtos de software e hardware projetados para se integrar perfeitamente à plataforma. Os drivers que foram criados para Windows Vista não devem exigir que a atualização seja executado corretamente no Windows 7. (Consulte [Windows Kit de Driver](/windows-hardware/drivers/).)

## <a name="devices"></a>Dispositivos

Windows 7 fornece suporte flexível e robusto para uma ampla variedade de aplicativos e dispositivos, incluindo players de música, dispositivos de armazenamento, telefones móveis e outros tipos de dispositivos conectados. O teste automático desses dispositivos é usado para garantir que os problemas de compatibilidade sejam corrigidos no início do ciclo de desenvolvimento. (Consulte [Windows conceitos básicos da classe de dispositivo](https://www.microsoft.com/whdc/device/default.mspx).)

## <a name="reliability-analysis-component"></a>Componente de análise de confiabilidade

O Componente de Análise de Confiabilidade é um agente nativo que fornece informações detalhadas da experiência do cliente com o uso e a confiabilidade do sistema. Essas informações são expostas por meio de uma interface WMI (Instrumentação de Gerenciamento do Windows) que as disponibilizam para consumo por Sistemas de Leitores Portáteis. Com a exposição do Componente de Análise de Confiabilidade por meio de uma interface WMI, os desenvolvedores podem monitorar e analisar seus aplicativos, aumentando a confiabilidade e o desempenho.

Windows 7 usa o Componente de Análise de Confiabilidade integrado para calcular um índice de confiabilidade que fornece informações sobre o uso geral do sistema e a estabilidade ao longo do tempo. O Componente de Análise de Confiabilidade também acompanha todas as alterações importantes do sistema que podem ter um impacto sobre a estabilidade, como atualizações do Windows e instalações de aplicativos. Você pode usar o snap-in do Monitor de Confiabilidade para ver tendências no índice de confiabilidade do sistema correlacionadas com esses eventos potencialmente desestabilizadores, facilitando o rastreamento de uma alteração de confiabilidade diretamente para um evento específico. (Consulte [Função MountVHD](/previous-versions/windows/desktop/msvs/mountvhd).)

 

 