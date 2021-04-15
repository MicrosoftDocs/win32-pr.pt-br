---
description: Se essa política do sistema por máquina for definida como um valor maior que 0, Windows Installer salvará versões mais antigas de arquivos em um cache quando um patch for aplicado a um aplicativo.
ms.assetid: 986cd521-6907-420d-a2e9-5e0da0069834
title: MaxPatchCacheSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8d9930f4a52d3ea0126a19d4dfadae359321f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461195"
---
# <a name="maxpatchcachesize"></a>MaxPatchCacheSize

Se essa [política do sistema](system-policy.md) por máquina for definida como um valor maior que 0, Windows Installer salvará versões mais antigas de arquivos em um cache quando um patch for aplicado a um aplicativo. O Caching pode aumentar o desempenho de instalações futuras que, de outra forma, precisam obter os arquivos antigos de uma fonte de aplicativo original.

O valor da política MaxPatchCacheSize é o percentual máximo de espaço em disco que o instalador pode usar para o cache de arquivos antigos. Por exemplo, um valor de 20 especifica no máximo 20% de uso. Se o tamanho total do cache atingir a porcentagem especificada de espaço em disco, nenhum arquivo adicional será salvo no cache. A política não afeta os arquivos que já foram salvos.

Se o valor da política MaxPatchCacheSize for definido como 0, nenhum arquivo adicional será salvo.

Se a política MaxPatchCacheSize não estiver definida, o valor padrão será 10 e um máximo de 10% do espaço em disco poderá ser usado para salvar arquivos antigos.

## <a name="registry-key"></a>Chave do Registro

**HKEY \_ \_** Políticas de \\ **software** do computador local \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de Dados

**REG \_ DWORD**

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sem suporte no Windows Installer 2,0 e versões anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



