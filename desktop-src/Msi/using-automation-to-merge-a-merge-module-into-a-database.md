---
description: os módulos de mesclagem fornecem um método padrão para fornecer componentes de Windows Installer compartilhados e configurar a lógica para aplicativos.
ms.assetid: 63ced106-12e3-4483-8bfe-22c54fe7a204
title: Usando a automação para mesclar um módulo de mesclagem em um banco de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 513a765670df44396c34537721eb6f75ed98796dd31ddefd5d26387e2a6b5d0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141325"
---
# <a name="using-automation-to-merge-a-merge-module-into-a-database"></a>Usando a automação para mesclar um módulo de mesclagem em um banco de dados

os [módulos de mesclagem](merge-modules.md) fornecem um método padrão para fornecer [*componentes*](c-gly.md)de Windows Installer compartilhados e configurar a lógica para aplicativos.

Os módulos de mesclagem devem ser mesclados em um pacote de instalação usando uma ferramenta de mesclagem. A prática recomendada é obter uma ferramenta de mesclagem distribuída livremente ou comprar uma das ferramentas de mesclagem que estão disponíveis de fornecedores de software independentes, por exemplo, você pode usar [Mergemod.dll](merge-module-automation.md).

o procedimento a seguir mostra como mesclar um módulo de mesclagem em um banco de dados Windows Installer usando a [automação do módulo de mesclagem](merge-module-automation.md).

**Para mesclar um módulo em um banco de dados**

1.  Abra um arquivo de log usando o método [**OpenLog**](merge-openlog.md) .

    Essa etapa será necessária somente se você precisar criar um arquivo de log ou acrescentar um arquivo de log existente para o processo de mesclagem.

2.  Abra o banco de dados de instalação do [.msi](windows-installer-file-extensions.md) usando o método [**OpenDatabase**](merge-opendatabase.md) do [**objeto Merge**](merge-object.md).

    Essa etapa é necessária.

    O banco de dados que você abre é aquele que você deseja receber o módulo de mesclagem.

3.  Abra o módulo de mesclagem [. msm](windows-installer-file-extensions.md) usando o método [**AbrirMódulo**](merge-openmodule.md) .

    Essa etapa é necessária.

    Este é o módulo de mesclagem que está sendo mesclado no banco de dados. Um módulo deve ser aberto antes que possa ser mesclado com um banco de dados de instalação.

4.  Mescle o módulo no banco de dados de instalação chamando o método [**Merge**](merge-object.md) ou o método [**MergeEx**](merge-mergeex.md) .

    Essa etapa é necessária.

    O método [**Merge**](merge-object.md) ou o método [**MergeEx**](merge-mergeex.md) só pode ser chamado uma vez para mesclar uma combinação específica de [.msi](windows-installer-file-extensions.md) e arquivos. msm.

    > [!Note]  
    > O método [**MergeEx**](merge-mergeex.md) só está disponível no [Mergemod.dll versão 2,0](merge-module-automation.md) ou posterior, e somente ao usar a interface [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) .

     

5.  Recupere a propriedade [**Errors**](merge-errors.md) e examine a coleção de objetos de [**erro**](error-object.md) que ele retorna para conflitos de mesclagem ou outros erros.

    Você deve resolver quaisquer erros.

    A recuperação não é destrutiva e várias instâncias da coleção de erros podem ser recuperadas com a leitura repetida da propriedade [**Errors**](merge-errors.md) .

6.  associe os componentes do módulo de mesclagem aos recursos usando o método [**Conexão**](merge-connect.md) .

    Esta etapa só será necessária se você tiver recursos existentes e quiser adicionar recursos para mesclar no banco de dados de instalação.

    Um recurso deve existir antes de você chamar esse método. Para obter mais informações, consulte [conectando um módulo de mesclagem a vários recursos](connecting-a-merge-module-to-multiple-features.md).

7.  Se necessário, extraia os arquivos de origem do módulo seguindo um ou mais destes procedimentos:
    -   Use [**ExtractFiles**](merge-extractfiles.md) ou [**ExtractFilesEx**](merge-extractfilesex.md) para extrair arquivos de um arquivo de .cab inserido e, em seguida, copiar para um diretório especificado.
        > [!Note]  
        > O [**ExtractFilesEx**](merge-extractfilesex.md) requer [Mergemod.dll versão 2,0](merge-module-automation.md) ou posterior.

         

    -   Use [**ExtractCAB**](merge-extractcab.md) para extrair arquivos de um arquivo de .cab inserido e, em seguida, salve em um arquivo especificado.
    -   Use [**CreateSourceImage**](merge-createsourceimage.md) para extrair arquivos de um módulo e, em seguida, após a mesclagem, copie para uma imagem de origem no disco.
        > [!Note]  
        > [**CreateSourceImage**](merge-createsourceimage.md) só está disponível no [Mergemod.dll versão 2,0](merge-module-automation.md) ou posterior.

         
8.  Feche o módulo de mesclagem aberto atual usando o método [**CloseModule**](merge-closemodule.md) .

    Essa etapa é necessária.

9.  Feche o banco de dados de instalação aberto usando o método [**CloseDatabase**](merge-closedatabase.md) .

    Essa etapa é necessária.

    Fechar um banco de dados limpa todas as informações de dependência, mas não afeta os erros que não são recuperados.

10. Feche o arquivo de log atual usando o método [**CloseLog**](merge-closelog.md) .

    Esta etapa será necessária se você tiver um arquivo de log aberto.

Depois que o módulo tiver sido mesclado no banco de dados usando [Mergemod.dll](merge-module-automation.md), a [tabela de mídia](media-table.md) deverá ser atualizada para descrever o layout da imagem de origem desejada. O processo de mesclagem fornecido pelo Mergemod.dll não atualiza a tabela de mídia porque o consumidor do módulo de mesclagem pode selecionar várias maneiras de fazer o layout da imagem de origem.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Versões, ferramentas e redistribuíveis liberados](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



