---
title: Usando informações de versão
description: Este tópico discute como usar as funções de informações de versão.
ms.assetid: 447b57c9-9e94-4a28-897e-f7b87d9cb25a
keywords:
- recursos, informações de versão
- informações de versão
- informações do arquivo de instalação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0447bc1dfc3b2d5d5006bb5ff9ca3e9fa8f3d488e9b5621acb932c843fc3630f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846986"
---
# <a name="using-version-information"></a>Usando informações de versão

Um programa de instalação normalmente tem os seguintes objetivos:

-   Para posicionar arquivos no local correto.
-   Para notificar o usuário se o programa de instalação está substituindo um arquivo existente por uma versão que seja significativamente diferente — por exemplo, substituindo um arquivo em idioma alemão por um arquivo em inglês ou substituindo um arquivo mais recente por um arquivo mais antigo.

Ao escrever o programa de instalação, você deve ter as seguintes informações para cada arquivo:

-   O nome e o local do arquivo (chamado de arquivo de origem).
-   O nome do arquivo equivalente no disco rígido do usuário (chamado de arquivo de destino). Esse nome é geralmente o mesmo que o nome de arquivo no disco de instalação.
-   O status de compartilhamento do arquivo — ou seja, se o arquivo é privado para o aplicativo que está sendo instalado ou pode ser compartilhado por vários aplicativos.

O programa de instalação pode usar a função [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea) para determinar onde o arquivo deve ser copiado no disco. Essa função também pode ser usada para especificar se o arquivo é privado para o aplicativo ou pode ser compartilhado. Se ocorrer um problema ao localizar o arquivo, **VerFindFile** retornará um valor de erro. Por exemplo, se o sistema estiver usando o arquivo de destino, **VerFindFile** retornará **VFF \_ FILEINUSE**. O programa de instalação deve notificar o usuário sobre o problema e responder à decisão do usuário para continuar ou para encerrar a instalação.

A função [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) copia o arquivo de origem para um arquivo temporário no diretório especificado por [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea). Se necessário, **VerInstallFile** expande o arquivo usando as funções na biblioteca de descompactação de dados.

[**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) compara as informações de versão do arquivo temporário para o do arquivo de destino. Se os dois forem diferentes, **VerInstallFile** retornará um ou mais valores de erro. Por exemplo, ele retornará **VIF \_ SRCOLD** se o arquivo temporário for mais antigo que o arquivo de destino e **VIF \_ DIFFLANG** se os arquivos tiverem identificadores de idioma ou valores de página de código diferentes. O programa de instalação deve notificar o usuário sobre o problema e responder à decisão do usuário para continuar ou para encerrar a instalação.

Alguns erros de [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) são recuperáveis. Ou seja, o programa de instalação pode chamar **VerInstallFile** novamente, especificando a opção **VIFF \_ forceinstall** , para instalar o arquivo, independentemente do conflito de versão. Se **VerInstallFile** retornar **VIF \_ tempfile** e o usuário optar por não forçar a instalação, o programa de instalação deverá excluir o arquivo temporário.

[**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) pode encontrar um erro não recuperável ao tentar forçar a instalação, mesmo que o erro não existisse anteriormente. Por exemplo, o arquivo pode ser bloqueado por outro usuário antes de o programa de instalação tentar forçar a instalação. Se um programa de instalação tentar forçar a instalação após um erro não recuperável, **VerInstallFile** falhará. O programa de instalação deve conter rotinas para se recuperar desse tipo de erro.

A solução recomendada é exibir uma caixa de diálogo com os botões **instalar**, **ignorar** e **instalar tudo**. (Outra solução é uma caixa de diálogo com os botões **Sim**, **Sim para todos**, **ignorar** e **Cancelar**.) O botão **instalar tudo** deve impedir que o programa de instalação solicite ao usuário erros semelhantes, incluindo a opção **VIFF \_ forceinstall** em todos os usos subsequentes de [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea). Para erros não recuperáveis, os botões **instalar** e **instalar tudo** devem ser desabilitados.

Para exibir uma mensagem de erro útil para o usuário, o programa de instalação geralmente deve recuperar informações dos recursos de versão dos arquivos conflitantes. Há quatro funções que o programa de instalação pode usar para essa finalidade:

-   [**Falha em GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea)
-   [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)
-   [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)
-   [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea)

[**Falha em GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) retorna o tamanho das informações de versão. [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa) usa informações recuperadas por **falha em GetFileVersionInfoSize** para recuperar uma estrutura que contém as informações de versão. [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea) recupera um membro específico dessa estrutura.

Por exemplo, se [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) retornar o **erro \_ VIF DiffType** , o programa de instalação deverá usar as funções [**falha em GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea), [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)e [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea) nos arquivos temporários e de destino para obter o tipo geral de cada arquivo. Se os idiomas dos arquivos entrarem em conflito, o programa de instalação também deverá usar o [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea) para converter o identificador de idioma binário em uma representação de texto do idioma. (Por exemplo, 0x040C é traduzido para a cadeia de caracteres "francês.")

Se [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) retornar um erro de arquivo, como **VIF \_ ACCESSVIOLATION**, o programa de instalação deverá usar a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) para recuperar o valor de erro mais recente. O programa deve converter esse valor em uma mensagem informativa para exibir para o usuário. O programa não deve produzir controle entre as chamadas para **VerInstallFile** e **GetLastError**.

 

 