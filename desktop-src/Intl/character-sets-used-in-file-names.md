---
description: O NTFS armazena nomes de arquivo em Unicode. Por outro lado, os sistemas de arquivos FAT12, FAT16 e FAT32 mais antigos usam o conjunto de caracteres OEM. Para obter mais informações, consulte Páginas de Código.
ms.assetid: 4573dd3b-ad68-460c-bc0f-ff65d4b70860
title: Conjuntos de caracteres usados em nomes de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dad9033b3ea723de757c59a73fc62c91a56da286ca74ca7444f31db42ff539f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107376"
---
# <a name="character-sets-used-in-file-names"></a>Conjuntos de caracteres usados em nomes de arquivo

O NTFS armazena nomes de arquivo em Unicode. Por outro lado, os sistemas de arquivos FAT12, FAT16 e FAT32 mais antigos usam o conjunto de caracteres OEM. Para obter mais informações, consulte [Páginas de Código](code-pages.md).

os aplicativos não-Unicode que criam arquivos FAT às vezes precisam usar as funções de conversão padrão da biblioteca de tempo de execução C para converter entre o conjunto de caracteres da página de código Windows e o conjunto de caracteres da página de código OEM. Com as implementações Unicode das funções do sistema de arquivos, não é necessário executar tais conversões.

seu aplicativo pode usar tipos de cadeia de caracteres genéricos, conforme descrito em [tipos de dados de Windows para cadeias](windows-data-types-for-strings.md). O aplicativo também pode usar protótipos de função genéricos usando técnicas descritas em [convenções para protótipos de função](conventions-for-function-prototypes.md). Para tipos de cadeia de caracteres genéricos ou protótipos de funções genéricas, seu aplicativo pode usar um único arquivo de origem para compilar uma versão Unicode ou não-Unicode. Para permitir isso, o aplicativo fornece macros para funções que não são invocadas durante a compilação para Unicode.

Nos sistemas de arquivos NTFS e Fat, os caracteres de nome de arquivo especiais são: ' \\ ', '/', '. ', '? ' e ' \* '. Em páginas de código OEM, esses caracteres especiais estão no intervalo ASCII de caracteres (0x00 a 0x7F). Seus equivalentes Unicode são os mesmos valores em um formato de 2 bytes, 0x0000 por meio de 0x007F.

> [!Caution]  
> Windows página de código e conjuntos de caracteres de página de código OEM usados em sistemas operacionais de idioma japonês contêm o símbolo de iene (¥) em vez de uma barra invertida ( \\ ). Portanto, o símbolo de Iene é um caractere proibido para sistemas de arquivos NTFS e FAT. Ao mapear o Unicode para uma página de código de idioma japonês, [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) e outras funções de conversão mapeiam ambas as barras invertidas (u + 005C) e o símbolo de iene Unicode normal (U + 00A5) para esse mesmo caractere. Por motivos de segurança, os aplicativos normalmente não devem permitir o caractere U + 00A5 em uma cadeia de caracteres Unicode que pode ser convertida para uso como um nome de arquivo FAT. Para obter mais informações, consulte [Considerações sobre segurança: recursos internacionais](security-considerations--international-features.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Unicode na API do Windows](unicode-in-the-windows-api.md)
</dt> <dt>

[Considerações sobre segurança: recursos internacionais](security-considerations--international-features.md)
</dt> </dl>

 

 



