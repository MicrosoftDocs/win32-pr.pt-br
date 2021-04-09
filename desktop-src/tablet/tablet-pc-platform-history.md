---
description: Esta seção descreve o histórico de versões da tecnologia do Tablet PC.
ms.assetid: 69eb161a-2330-456f-b7b8-234cf02c8b58
title: Histórico da plataforma do Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f258876f79f8e701ed59242233dcccc292b15f52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011683"
---
# <a name="tablet-pc-platform-history"></a>Histórico da plataforma do Tablet PC

Esta seção descreve o histórico de versões da tecnologia do Tablet PC.

## <a name="platform-description"></a>Descrição da plataforma

Os componentes de tecnologia do Tablet PC permitem desenvolver aplicativos projetados para hardware de Tablet PC.

Esses componentes podem ser usados para criar aplicativos que são executados no Windows XP Tablet PC Edition 2005, no Windows Vista, no Windows 7, no Windows Server 2008 R2 e em alguns outros sistemas operacionais anteriores.

O Windows Presentation Foundation também dá suporte ao desenvolvimento de aplicativos do Tablet PC.

## <a name="version-history"></a>Histórico de versão

### <a name="tablet-platform-in-windows-7-and-windows-server-2008-r2"></a>Plataforma Tablet no Windows 7 e no Windows Server 2008 R2

O Windows 7 apresenta suporte a idiomas adicionais, controle de entrada de matemática e dicionários personalizados. Os recursos do [Windows Touch](../wintouch/windows-touch-portal.md) também foram adicionados aos sistemas operacionais Windows.

O Windows Server 2008 R2 apresenta suporte para idiomas adicionais, dicionários personalizados e reconhecimento do lado do servidor.

Os recursos a seguir aprimoram a funcionalidade do Tablet e permitem que os desenvolvedores forneçam novos aplicativos que dão suporte a cenários práticos para usuários finais.

-   O controle de entrada de matemática permite a entrada de fórmulas e funções matemáticas de texto manuscrito no Windows 7.
-   Em um esforço para melhorar o reconhecimento de texto, o Windows 7 e o Windows Server 2008 R2 dão suporte a dicionários personalizados para que os administradores possam habilitar diretamente o suporte para listas de palavras.
-   O Windows Touch dá suporte à entrada de várias fontes de toque por meio de novas mensagens de janela, além de uma API de reconhecimento de gesto que dá suporte a movimento panorâmico, zoom e rotação.
-   O Windows Server 2008 R2 dá suporte ao reconhecimento do lado do servidor da entrada de formulário e também dá suporte a dicionários personalizados para reconhecimento do lado do servidor. Com a adição desses recursos, os desenvolvedores e administradores podem criar e personalizar aplicativos poderosos que dão suporte ao reconhecimento de manuscrito do lado do servidor.

### <a name="tablet-platform-in-windows-vista"></a>Plataforma Tablet no Windows Vista

Os binários de tecnologia do Tablet PC foram atualizados no Windows Vista. A tecnologia do Tablet PC atualizada inclui novas APIs de análise de tinta e uma versão COM das APIs de entrada da caneta. Os aplicativos escritos em relação às versões anteriores da tecnologia do Tablet PC são executados no Windows Vista sem modificação.

Os componentes de tecnologia do Tablet PC estão disponíveis apenas como parte do SDK do Windows a partir do lançamento do Windows Vista. Para obter mais informações, consulte [o que há de novo no desenvolvimento do Tablet PC](what-s-new-in-tablet-pc-development.md).

### <a name="version-17"></a>Versão 1,7

O Tablet PC Development Kit 1,7 ampliou a funcionalidade de desenvolvimento além da disponível na versão 1,5, adicionando as APIs de entrada da caneta e o suporte para tinta na Web.

No passado, a funcionalidade da versão 1,5 estava em um binário separado, mas no kit de desenvolvimento do Tablet PC 1,7, toda a funcionalidade foi colocada em um único binário.

### <a name="version-15"></a>Versão 1.5

A versão 1,5 do kit de desenvolvimento substituiu a versão 1,1. Ele forneceu APIs do painel de entrada de caneta e o objeto divisória.

> [!Note]  
> Se você instalar o kit de desenvolvimento do Tablet PC versão 1,5, após a instalação, você deverá restabelecer as referências ao assembly do Microsoft Ink em aplicativos escritos em relação às versões anteriores do SDK do Tablet PC antes de compilar e executar.

 

### <a name="version-11"></a>Versão 1.1

A versão 1,1 do kit de desenvolvimento substituiu a versão 1,0. A versão 1,1 consistiu unicamente de atualizações na documentação; os binários de plataforma não foram alterados entre a versão 1,1 do kit de desenvolvimento e a versão de lançamento do Windows XP Tablet PC Edition. Portanto, os aplicativos desenvolvidos no kit de desenvolvimento da versão 1,1 não precisam redistribuir nenhum componente para usar os recursos de plataforma quando instalados em Tablet PCs.

> [!Note]  
> Os aplicativos que estão sendo distribuídos para sistemas operacionais não Tablet PC podem usar um subconjunto dos recursos da plataforma Tablet PC. Esses aplicativos devem incluir o módulo de mesclagem redistribuída fornecido no kit de desenvolvimento da versão 1,1 com sua configuração.

 

### <a name="version-10"></a>Versão 1.0

A versão 1,0 do kit de desenvolvimento foi substituída pela versão 1,1.

 

 
