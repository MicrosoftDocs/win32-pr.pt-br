---
description: Se o compilador MOF não puder concluir a compilação de um arquivo MOF, o repositório do WMI poderá ser deixado em um estado indefinido.
ms.assetid: 13adc666-6588-4cfd-a5eb-17da93434468
ms.tgt_platform: multiple
title: Tratamento de erros com o compilador MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905b406020787de894a2821b501ee465ab63ea5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461334"
---
# <a name="handling-errors-with-the-mof-compiler"></a>Tratamento de erros com o compilador MOF

Se o compilador MOF não puder concluir a compilação de um arquivo MOF, o repositório do WMI poderá ser deixado em um estado indefinido. Por exemplo, se você estiver Compilando um arquivo MOF e usar a opção de linha de comando **-Class: createonly** , a compilação será encerrada se uma classe especificada no arquivo MOF já existir. O compilador MOF armazena no repositório quaisquer classes ou instâncias que foram definidas até o ponto em que o compilador pára. Em alguns casos, isso pode deixar o repositório WMI em uma condição indefinida.

Nessa situação, talvez seja necessário parar o WMI, excluir o repositório WMI e fazer com que o WMI o recrie. Todos os arquivos MOF que contêm o comando [**pragma AutoRecuperação**](pragma-autorecover.md) do [pré-processador](preprocessor-commands.md) são recriados quando o WMI é reiniciado. Você deve recompilar manualmente todos os arquivos MOF que não incluem uma `#pragma autorecover` instrução.

Para obter mais informações sobre como declarar classes e instâncias usando a sintaxe do MOF, consulte [Designing formato MOF (MOF) classes](designing-managed-object-format--mof--classes.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Compilando arquivos MOF](compiling-mof-files.md)
</dt> <dt>

[**Mofcomp**](mofcomp.md)
</dt> <dt>

[Comandos de pré-processador](preprocessor-commands.md)
</dt> </dl>

 

 



