---
description: Os desenvolvedores criam um pacote de patch gerando um arquivo de criação de patch e usando Msimsp.exe para chamar a função UiCreatePatchPackageEx no Patchwiz.dll.
ms.assetid: 8a163653-6ba1-46ea-9832-f998749d29ae
title: Criando um pacote de patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2d784e02374eeee84a0c8b047e5a7b4db31f9c2b3090a68c31f35dece8c978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638286"
---
# <a name="creating-a-patch-package"></a>Criando um pacote de patch

Os desenvolvedores criam um pacote de patch gerando um arquivo de criação de patch e [ usandoMsimsp.exe](msimsp-exe.md) para chamar a [função UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) [ noPatchwiz.dll](patchwiz-dll.md). Msimsp.exe e Patchwiz.dll são fornecidos no SDK Windows Installer. Para obter mais informações, consulte [Um pequeno exemplo de a](a-small-update-patching-example.md)patch de atualização .

Como a aplicação de um patch a um pacote do instalador do Windows resulta na instalação das fontes originais usando um novo arquivo .msi, o novo arquivo .msi deve permanecer compatível com o layout da origem original.

Ao criar um pacote de patch, você deve usar uma imagem de instalação descompactada para criar um patch, por exemplo, uma imagem administrativa ou uma imagem de instalação descompactada de um CD-ROM. Você também deve seguir as seguintes restrições:

-   Não mova arquivos de uma pasta para outra.
-   Não mova arquivos de um gabinete para outro.
-   Não altere a ordem dos arquivos em um gabinete.
-   Não altere o número de sequência de arquivos existentes. O número da sequência é o valor especificado na coluna Sequência da [Tabela de Arquivos](file-table.md).
-   Todos os novos arquivos adicionados pelo patch devem ser colocados no final da sequência de arquivos existente. O número de sequência de qualquer novo arquivo na imagem atualizada deve ser maior que o maior número de sequência de arquivos existentes na imagem de destino.
-   Não altere as chaves primárias na Tabela [de Arquivos](file-table.md) entre as versões de arquivo .msi original e nova.
    > [!Note]  
    > O arquivo deve ter a mesma chave na Tabela [de](file-table.md) Arquivos da imagem de destino e da imagem atualizada. Os valores de cadeia de caracteres na coluna Arquivo de ambas as tabelas devem ser idênticos, incluindo o caso.

     

-   Não autor de um pacote com chaves [de Tabela](file-table.md) de Arquivos que diferem apenas caso, por exemplo, evite o exemplo de tabela a seguir.

    

    | Arquivo       | Componente\_ | FileName   |
    |------------|-------------|------------|
    | readme.txt | Comp1       | readme.txt |
    | ReadMe.txt | Comp2       | readme.txt |

    

     

    O instalador Windows pode permitir o exemplo de tabela anterior quando Comp1 e Comp2 estão instalados em diretórios diferentes, mas você não pode usar [Msimsp.exe](msimsp-exe.md) [ouPatchwiz.dll](patchwiz-dll.md) para gerar um patch para o pacote. Msimsp.exe e Patchwiz.dll chamada Makecab.exe, que não faz maiúsculas de minúsculas e falha.

    Ao usar módulos de mesclagem na configuração, verifique se os números de sequência de arquivos e o layout aderem às diretrizes acima.

 

 



