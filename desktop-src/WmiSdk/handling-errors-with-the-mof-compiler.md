---
description: Se o compilador MOF não puder concluir a compilação de um arquivo MOF, o repositório WMI poderá ser deixado em um estado indefinido.
ms.assetid: 13adc666-6588-4cfd-a5eb-17da93434468
ms.tgt_platform: multiple
title: Tratamento de erros com o compilador MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03f5174af836a0b27824c40486364cc81809db97b9608e6b1c813c4c1029d3aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993166"
---
# <a name="handling-errors-with-the-mof-compiler"></a>Tratamento de erros com o compilador MOF

Se o compilador MOF não puder concluir a compilação de um arquivo MOF, o repositório WMI poderá ser deixado em um estado indefinido. Por exemplo, se você estiver compilando um arquivo MOF e usar a opção de linha de comando **-class:createonly,** a compilação será encerrada se uma classe especificada no arquivo MOF já existir. O compilador MOF armazena no repositório quaisquer classes ou instâncias que foram definidas até o ponto em que o compilador para. Em alguns casos, isso pode deixar o repositório WMI em uma condição indefinida.

Nessa situação, talvez seja necessário interromper o WMI, excluir o repositório WMI e recomerá-lo. Todos os arquivos MOF que contêm o comando de [pré-processador](preprocessor-commands.md) [**pragma autorecover**](pragma-autorecover.md) são reconstruídos quando o WMI é reiniciado. Você deve recompilá-los manualmente quaisquer arquivos MOF que não incluam uma `#pragma autorecover` instrução .

Para obter mais informações sobre como declarar classes e instâncias usando a sintaxe MOF, consulte [Designando classes Managed Object Format (MOF).](designing-managed-object-format--mof--classes.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Compilando arquivos MOF](compiling-mof-files.md)
</dt> <dt>

[**mofcomp**](mofcomp.md)
</dt> <dt>

[Comandos de pré-processador](preprocessor-commands.md)
</dt> </dl>

 

 



