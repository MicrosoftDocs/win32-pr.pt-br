---
description: se essa política do sistema por máquina for definida como um valor maior que 0, Windows Installer salvará versões mais antigas de arquivos em um cache quando um patch for aplicado a um aplicativo.
ms.assetid: 986cd521-6907-420d-a2e9-5e0da0069834
title: MaxPatchCacheSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85291977073d1ab65c43ce9c4307e7c97519133330769e56c4b9dc7a883972dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013054"
---
# <a name="maxpatchcachesize"></a>MaxPatchCacheSize

se essa [política do sistema](system-policy.md) por máquina for definida como um valor maior que 0, Windows Installer salvará versões mais antigas de arquivos em um cache quando um patch for aplicado a um aplicativo. Caching pode aumentar o desempenho de instalações futuras que, de outra forma, precisam obter os arquivos antigos de uma fonte de aplicativo original.

O valor da política MaxPatchCacheSize é o percentual máximo de espaço em disco que o instalador pode usar para o cache de arquivos antigos. Por exemplo, um valor de 20 especifica no máximo 20% de uso. Se o tamanho total do cache atingir a porcentagem especificada de espaço em disco, nenhum arquivo adicional será salvo no cache. A política não afeta os arquivos que já foram salvos.

Se o valor da política MaxPatchCacheSize for definido como 0, nenhum arquivo adicional será salvo.

Se a política MaxPatchCacheSize não estiver definida, o valor padrão será 10 e um máximo de 10% do espaço em disco poderá ser usado para salvar arquivos antigos.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer** de políticas de Software de computador LOCAL

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



