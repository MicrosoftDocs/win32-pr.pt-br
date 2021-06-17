---
description: 'Você tem duas opções ao compilar um arquivo MOF: usando o utilitário de linha de comando ou usando uma interface programática.'
ms.assetid: 1760f1bd-7027-4201-97a2-ca902f945b52
ms.tgt_platform: multiple
title: Executando o compilador MOF em um arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f62834944e995c3e7f3763c460d72f9f70aa66
ms.sourcegitcommit: 7eadd92b1da5eb4eab7d516a5a768e7f7fc02d4c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/16/2021
ms.locfileid: "112230233"
---
# <a name="running-the-mof-compiler-on-a-file"></a>Executando o compilador MOF em um arquivo

Você tem duas opções ao compilar um arquivo MOF: usando o utilitário de linha de comando ou usando uma interface programática.

Até que você execute o compilador MOF, [**Mofcomp.exe**](mofcomp.md), um provedor não está registrado com o WMI e as classes criadas no arquivo MOF não estão disponíveis no [*repositório WMI*](gloss-w.md). O procedimento a seguir descreve como compilar um arquivo MOF.

**Para executar o compilador MOF em um arquivo da linha de comando**

1.  Chame o compilador MOF na linha de comando, usando a sintaxe a seguir.

    **Mofcomp** _MOFfile_**. mof**

    O compilador MOF dá suporte a uma variedade de opções para controlar situações de processamento especiais. Todas as opções são opcionais e qualquer combinação de opções é permitida. No entanto, não faz sentido usar alguns dos comutadores em combinação com outros. Por exemplo, para combinar as opções **-Class: UpdateOnly** e **-Class: createonly** , os resultados do compilador não executam nenhuma ação.

    Por padrão, o Mofcomp.exe armazena as classes compiladas no \\ namespace WMI padrão raiz. Observe que o namespace padrão para Mofcomp.exe não é o mesmo que o namespace padrão para scripts. O namespace padrão para scripts é especificado no controle WMI na guia Avançado. Para obter mais informações, consulte [definindo a segurança do namespace com o controle WMI](setting-namespace-security-with-the-wmi-control.md).

    Você pode alterar o namespace que recebe as classes de duas maneiras.

    1.  Use a opção **-N** para o comando **Mofcomp** .
    2.  Insira o namespace de pragma do comando de pré-processador \# [](pragma-namespace.md) no arquivo MOF.

2.  Opcionalmente, você pode compilar um arquivo MOF programaticamente. Para obter mais informações, consulte [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Compilando arquivos MOF](compiling-mof-files.md)
</dt> <dt>

[**Mofcomp**](mofcomp.md)
</dt> <dt>

[Comandos de pré-processador](preprocessor-commands.md)
</dt> </dl>

 

 



