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

Os desenvolvedores criam um pacote de patch gerando um arquivo de criação de patch e usando [Msimsp.exe](msimsp-exe.md) para chamar a função [UiCreatePatchPackageEx](uicreatepatchpackageex--patchwiz-dll-.md) no [Patchwiz.dll](patchwiz-dll.md). Msimsp.exe e Patchwiz.dll são fornecidos no SDK do Windows Installer. Para obter mais informações, consulte [um exemplo de aplicação de patch de atualização pequena](a-small-update-patching-example.md).

como o aplicativo de um patch para um pacote de Windows Installer resulta na instalação das fontes originais usando um novo arquivo de .msi, o novo arquivo de .msi deve permanecer compatível com o layout da fonte original.

Quando você cria um pacote de patch, deve usar uma imagem de instalação descompactada para criar um patch, por exemplo, uma imagem administrativa ou uma imagem de instalação descompactada de um CD-ROM. Você também deve aderir às seguintes restrições:

-   Não mova arquivos de uma pasta para outra.
-   Não mova arquivos de um gabinete para outro.
-   Não altere a ordem dos arquivos em um gabinete.
-   Não altere o número de sequência de arquivos existentes. O número de sequência é o valor especificado na coluna sequência da [tabela de arquivos](file-table.md).
-   Todos os novos arquivos adicionados pelo patch devem ser colocados no final da sequência de arquivos existente. O número de sequência de qualquer arquivo novo na imagem atualizada deve ser maior que o maior número de sequência de arquivos existentes na imagem de destino.
-   Não altere as chaves primárias na [tabela de arquivos](file-table.md) entre as versões original e nova .msi arquivo.
    > [!Note]  
    > O arquivo deve ter a mesma chave na [tabela de arquivos](file-table.md) da imagem de destino e da imagem atualizada. Os valores de cadeia de caracteres na coluna arquivo de ambas as tabelas devem ser idênticos, incluindo o caso.

     

-   Não crie um pacote com chaves de [tabela de arquivos](file-table.md) que diferem apenas em maiúsculas e minúsculas, por exemplo, evite o exemplo de tabela a seguir.

    

    | Arquivo       | Componente\_ | FileName   |
    |------------|-------------|------------|
    | readme.txt | Comp1       | readme.txt |
    | ReadMe.txt | Comp2       | readme.txt |

    

     

    o Windows Installer pode permitir o exemplo de tabela anterior quando Comp1 e Comp2 são instalados em diretórios diferentes, mas você não pode usar [Msimsp.exe](msimsp-exe.md) ou [Patchwiz.dll](patchwiz-dll.md) para gerar um patch para o pacote. Msimsp.exe e Patchwiz.dll chamada Makecab.exe, que não diferencia maiúsculas de minúsculas e falha.

    Ao usar módulos de mesclagem na configuração, verifique se os números de sequência de arquivo e o layout aderem às diretrizes acima.

 

 



