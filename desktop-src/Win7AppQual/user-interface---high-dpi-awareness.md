---
description: Interface do usuário – reconhecimento de DPI alto
ms.assetid: 5b753340-366c-44b3-87e9-19c580f1c5d5
title: Interface do usuário – reconhecimento de DPI alto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 118b566d35f753a77f6cfd9706c2e69819f3fbaa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116064"
---
# <a name="user-interface---high-dpi-awareness"></a>Interface do usuário – reconhecimento de DPI alto

## <a name="affected-platforms"></a>Plataformas afetadas

 **Clientes** -Windows XP Windows \| Vista Windows \| 7  

## <a name="feature-impact"></a>Impacto do recurso

**Severidade** -média  
**Frequência** -média  

## <a name="description"></a>Descrição

O objetivo é incentivar os usuários finais a definir seus monitores para resolução nativa e usar DPI em vez de resolução de tela para alterar o tamanho do texto e das imagens exibidas. O Windows 7 pode detectar e configurar automaticamente um DPI padrão em instalações limpas em computadores configurados por seus OEMs usando configurações de DPI. Há ferramentas que você pode usar para ajudar a criar aplicativos com reconhecimento de DPI alto para garantir os resultados mais legíveis.

Adicionamos dois novos recursos de DPI alto ao Windows 7:

-   Configuração de DPI por usuário (anteriormente por computador)
-   Alterar DPI sem reinicialização (o logoff/logon ainda é necessário)

## <a name="manifestation-of-impact"></a>Manifestação do impacto

Os aplicativos que não manipulam o caso de DPI alto provavelmente apresentarão artefatos visuais, incluindo:

-   Recorte da interface do usuário ou do texto por outros elementos da interface do usuário
-   Tamanhos de fonte inconsistentes
-   UIs fora da tela
-   Desfoque do texto ou da interface do usuário
-   Arrastar e soltar desfeito ou outras entradas
-   Renderização de aplicativos DX de tela inteira parcialmente fora da tela

## <a name="solution"></a>Solução

Para tornar seus aplicativos cientes de DPI:

1.  Faça um passo de teste funcional de alto nível, incluindo instalar e desinstalar nas seguintes configurações:

    | Configuração                                              | O que procurar                                                                                                                                                      |
    |------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | 1024x768 @ 120 DPI (125% de dimensionamento)                    | Essa é uma resolução efetiva de ~ 800x600, então procure a interface do usuário recortada da tela ou dos problemas de layout. Procure também bitmaps do pixilated & ícones.                         |
    | @144dpi 1600x1200 (150% de dimensionamento)                    | Interface do usuário borrada. Verifique se todas as operações do mouse funcionam, especialmente arraste & operações drop. Verifique também se os modos de tela inteira funcionam corretamente.                                     |
    | 1600x1200 @ 144 DPI com virtualização de DPI desabilitada | Frequentemente, os botões e a interface do usuário não serão dimensionados em relação ao texto maior & haverá um recorte de texto significativo. Procure problemas de layout em geral & pixilated bitmats & ícones. |

    

     

2.  Anote todos os problemas encontrados, incluindo a localização, a resolução da tela e as configurações de DPI, além de como o aplicativo se comporta nas outras configurações de DPI/resolução para fins de integridade
3.  Verificar cada problema em relação aos problemas comuns de codificação de DPI
4.  Avaliar o custo de fazer com que o aplicativo reconheça totalmente o DPI
5.  Faça uma lista dos ativos de DPI alto necessários (por exemplo, botões, ícones)
6.  Solucionar e corrigir a lista de problemas de DPI encontrados na etapa 1
7.  Integre os novos ativos da etapa 5
8.  Declarar o reconhecimento de DPI de aplicativo

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Compatibilidade, desempenho, confiabilidade e teste de usabilidade

Execute novamente a avaliação de reconhecimento de DPI e verifique se os problemas foram corrigidos.

## <a name="links-to-other-resources"></a>Links para outros recursos

-   [Desenvolvimento de aplicativos de desktop de alto DPI no Windows](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   **Contate as perguntas técnicas:**<disup@microsoft.com>

 

 
