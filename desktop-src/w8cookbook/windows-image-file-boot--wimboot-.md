---
title: Windows Inicialização de arquivo de imagem (WimBoot)
description: Windows Inicialização de arquivo de imagem (WimBoot)
ms.assetid: 1C4EFC42-6698-4981-8C55-D1DFC6309F31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 687a230188c3b13317d8176d8209cf5e38026c3b6f161be7ffe0c2ed760976ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119932116"
---
# <a name="windows-image-file-boot-wimboot"></a>Windows Inicialização de arquivo de imagem (WimBoot)

## <a name="platform"></a>Plataforma

**Clientes:** Windows 8.1  

## <a name="description"></a>Descrição

O WimBoot é uma maneira alternativa para os OEMs implantarem Windows. Uma implantação do WimBoot é inicializada e Windows diretamente de um WIM (arquivo de imagem Windows) compactado. Esse arquivo WIM é imutável e o acesso a ele é gerenciado por um novo driver de filtro do sistema de arquivos (WoF.sys).

O resultado é uma redução significativa no espaço em disco necessário para instalar Windows.

## <a name="manifestations"></a>Manifestações

A maioria dos aplicativos não deve ser completamente afetada pelo WimBoot. Somente aplicativos que acessam e desbloqueia arquivos do sistema ou arquivos pré-carregados para acesso de gravação podem ser afetados. Como o WIM é imutável, as atualizações nele (ou seja, arquivos pré-carregados ou do sistema) são simplesmente armazenadas na partição \\ C:.

Se um aplicativo desbloqueou o acesso de gravação para todos os arquivos pré-carregados e sistema com suporte de WIM, a economia que o WimBoot oferece seria completamente perdida, pois todos esses arquivos seriam descompactados e colocados no \\ volume C:.

Além disso, os aplicativos de backup e restauração precisam estar cientes das implantações do WimBoot, pois o WIM está presente em uma partição separada; ou seja, no back-up, as partições C: e WIM devem ser salvas e ambas \\ devem ser restauradas juntas.

## <a name="solution"></a>Solução

Novas APIs foram introduzidas que permitem que os aplicativos consultem diretamente se um determinado volume ou arquivo é apoiado por um WIM. Essas informações permitem que os aplicativos tomam decisões apropriadas, como abrir esses arquivos apenas para acesso de leitura ou para identificar volumes/partições que devem ser armazenados em backup e restaurados juntos.

## <a name="compatibility-performance-reliability-or-usability-tests"></a>Testes de compatibilidade, desempenho, confiabilidade ou usabilidade

Os desenvolvedores de aplicativos devem testar seu software e seus cenários correspondentes em um sistema WimBoot, especialmente se esses aplicativos acessam o sistema ou arquivos pré-carregados. É preciso ter atenção especial para uma redução significativa no espaço em disco disponível após a conclusão de um cenário.

 

 




