---
description: os módulos de mesclagem fornecem um método padrão para que os desenvolvedores forneçam componentes de Windows Installer compartilhados e a lógica de instalação para seus aplicativos.
ms.assetid: 3eb087b1-0f44-40d8-a950-67d489f09408
title: Usando a API para mesclar um módulo de mesclagem em um banco de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdbeb68b193cceff10fbd1cd3f56f4c8804a4e1fb4f7c169fd2d893dc0b4bfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039026"
---
# <a name="using-the-api-to-merge-a-merge-module-into-a-database"></a>Usando a API para mesclar um módulo de mesclagem em um banco de dados

os [módulos de mesclagem](merge-modules.md) fornecem um método padrão para que os desenvolvedores forneçam [*componentes*](c-gly.md) de Windows Installer compartilhados e a lógica de instalação para seus aplicativos. Os módulos de mesclagem devem ser mesclados em um pacote de instalação usando uma ferramenta de mesclagem. A melhor alternativa é obter uma ferramenta de mesclagem distribuída livremente ou comprar uma das ferramentas de mesclagem disponíveis de fornecedores de software independentes. Por exemplo, você pode usar a funcionalidade fornecida pelo [Mergemod.dll](merge-module-automation.md).

Use as etapas a seguir em sequência para mesclar um módulo de mesclagem em um Windows Installer banco de dados de instalação pela API do [Mergemod.dll](merge-module-automation.md).

**para mesclar um módulo de mesclagem em um Windows Installer banco de dados de instalação**

1.  Abra um arquivo de log usando [**OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog). Essa etapa será necessária somente se você precisar criar um arquivo de log ou acrescentar um arquivo de log existente para o processo de mesclagem.
2.  Abra o banco de dados de instalação, um [ arquivo.msi](windows-installer-file-extensions.md), que receberá o módulo de mesclagem usando [**OpenDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-opendatabase). Essa etapa é necessária.
3.  Abra o módulo de mesclagem, um [arquivo. msm](windows-installer-file-extensions.md), que está sendo mesclado no banco de dados usando [**AbrirMódulo**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule). Um módulo deve ser aberto antes que possa ser mesclado com um banco de dados de instalação. Essa etapa é necessária.
4.  Mescle o módulo no banco de dados de instalação usando [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) ou [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex). Observe que **Merge** ou **MergeEx** só podem ser chamados uma vez para mesclar uma combinação específica de .msi e arquivos. msm. **MergeEx** só está disponível ao usar [Mergemod.dll versão 2,0](merge-module-automation.md) ou posterior e somente ao usar a interface [IMsmMerge2](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) . Essa etapa é necessária.
5.  Chame [**\_ erros Get**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-get_errors) e examine a coleção de erros recuperada para conflitos de mesclagem ou outros erros. A recuperação não é destrutiva. Várias instâncias da coleção de erros podem ser recuperadas com a leitura repetida de **\_ erros Get** de chamada. Você precisará resolver todos os erros conforme apropriado para seu caso.
6.  associe os componentes do módulo de mesclagem a todos os recursos adicionais que foram, ou serão, mesclados no banco de dados de instalação usando [**Conexão**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect). O recurso já deve existir antes de chamar este método. Esta etapa só será necessária se você tiver recursos adicionais. para obter mais informações, consulte [conectando um módulo de mesclagem a vários recursos](connecting-a-merge-module-to-multiple-features.md)
7.  Se necessário, extraia os arquivos de origem do módulo seguindo um ou mais dos procedimentos a seguir.

    Para extrair arquivos de um arquivo de .cab inserido e, em seguida, copiar para um diretório especificado, use [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) ou [**ExtractFilesEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex). Observe que o **ExtractFilesEx** requer [Mergemod.dll versão 2,0](merge-module-automation.md) ou posterior.

    Para extrair arquivos de um arquivo de .cab inserido e, em seguida, salvar em um arquivo especificado, use [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab).

    Para extrair arquivos de um módulo e, em seguida, copiar para uma imagem de origem no disco após a mesclagem, use [**CreateSourceImage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage). Observe que o **CreateSourceImage** só está disponível com [Mergemod.dll versão 2,0](merge-module-automation.md) ou posterior.

8.  Feche o módulo de mesclagem aberto atual usando [**CloseModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule). Essa etapa é necessária.
9.  Feche o banco de dados de instalação aberta atual usando o [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase). Essa etapa é necessária. Fechar um banco de dados limpa todas as informações de dependência, mas não afeta os erros que não foram recuperados.
10. Feche o arquivo de log atual usando [**CloseLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closelog). Essa etapa será necessária se você tiver aberto um arquivo de log.

Depois que o módulo tiver sido mesclado no banco de dados usando [Mergemod.dll](merge-module-automation.md), a [tabela de mídia](media-table.md) deverá ser atualizada para descrever o layout da imagem de origem desejada. O processo de mesclagem fornecido pelo Mergemod.dll não atualiza a tabela de mídia porque o consumidor do módulo de mesclagem pode selecionar várias maneiras de fazer o layout da imagem de origem.

 

 
