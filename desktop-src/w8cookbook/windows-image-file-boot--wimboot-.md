---
title: Inicialização do arquivo de imagem do Windows (WimBoot)
description: Inicialização do arquivo de imagem do Windows (WimBoot)
ms.assetid: 1C4EFC42-6698-4981-8C55-D1DFC6309F31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f14ea506226e2c16d771ecec52fa31a8c871b4
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "103642935"
---
# <a name="windows-image-file-boot-wimboot"></a>Inicialização do arquivo de imagem do Windows (WimBoot)

## <a name="platform"></a>Plataforma

**Clientes:** Windows 8.1  

## <a name="description"></a>Descrição

O WimBoot é uma maneira alternativa para os OEMs implantarem o Windows. Uma implantação do WimBoot é inicializada e executa o Windows diretamente de um arquivo compactado de imagem do Windows (WIM). Esse arquivo WIM é imutável e o acesso a ele é gerenciado por um novo driver de filtro do sistema de arquivos (WoF.sys).

O resultado é uma redução significativa no espaço em disco necessário para instalar o Windows.

## <a name="manifestations"></a>Manifestações

A maioria dos aplicativos deve ser completamente não afetada pelo WimBoot. Somente os aplicativos que acessam e desbloqueiam arquivos do sistema ou arquivos pré-carregados para acesso de gravação podem ser afetados. Como o WIM é imutável, as atualizações para ele (ou seja, arquivos do sistema ou pré-carregados) são simplesmente armazenadas na partição C: \\ .

Se um aplicativo desbloqueou o acesso de gravação para todo o sistema com suporte para WIM e arquivos pré-carregados, a economia que o WimBoot fornece será completamente perdida, pois todos esses arquivos seriam descompactados e colocados no volume C: \\ .

Além disso, os aplicativos de backup e restauração precisam estar cientes das implantações do WimBoot, já que o WIM está presente em uma partição separada; ou seja, em backup, as partições C: \\ e Wim devem ser salvas e ambas devem ser restauradas juntas.

## <a name="solution"></a>Solução

Foram introduzidas novas APIs que permitem que os aplicativos consultem diretamente se um determinado volume ou arquivo é apoiado por um WIM. Essas informações permitem que os aplicativos tomem decisões apropriadas, como abrir esses arquivos somente para acesso de leitura ou para identificar volumes/partições que precisam ser armazenados em backup e restaurados juntos.

## <a name="compatibility-performance-reliability-or-usability-tests"></a>Compatibilidade, desempenho, confiabilidade ou testes de usabilidade

Os desenvolvedores de aplicativos devem testar seu software e seus cenários correspondentes em um sistema WimBoot, especialmente se esses aplicativos acessarem arquivos de sistema ou pré-carregados. A atenção especial deve ser paga a uma redução significativa no espaço em disco disponível após a conclusão de um cenário.

 

 




