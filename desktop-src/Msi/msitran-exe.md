---
description: Msitran.exe usa MsiDatabaseGenerateTransform, MsiCreateTransformSummaryInfo e MsiDatabaseApplyTransform para gerar ou aplicar um arquivo de transformação. Essa ferramenta só está disponível nos componentes SDK do Windows para desenvolvedores de Windows Installer.
ms.assetid: cfc7b907-78d7-4a78-bab4-ede9012d5a36
title: Msitran.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a69936155fb3880f43e0f7563bc6aabd59f53703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759211"
---
# <a name="msitranexe"></a>Msitran.exe

Msitran.exe usa [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma), [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)e [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) para gerar ou aplicar um arquivo de transformação.

Essa ferramenta só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="syntax"></a>Sintaxe

Use a sintaxe a seguir para gerar uma transformação.

**msitran-g** *{banco de dados base} {REF DB} {nome do arquivo de transformação} \[ {condições de \] erro/condições de validação}*

Use a sintaxe a seguir para aplicar uma transformação

**msitran-a** *{Transform} {banco de dados} \[ {condições \] de erro}*

## <a name="command-line-options"></a>Opções de linha de comando

Msitran.exe usa as seguintes opções de linha de comando que não diferenciam maiúsculas de minúsculas. Um delimitador de barra também pode ser usado no lugar de um traço.



| Opção | Descrição            |
|--------|------------------------|
| -g     | Geração de transformação.  |
| -a     | Aplicativo de transformação. |



 

Os erros a seguir podem ser suprimidos ao aplicar uma transformação. Para suprimir um erro, inclua o caractere apropriado no argumento {Error Conditions}. As condições especificadas com-g são colocadas nas informações resumidas da transformação, mas não são usadas ao aplicar uma transformação com-a. Para obter informações, consulte [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma).



| Opção | Erro suprimido           |
|--------|----------------------------|
| um      | Adicionar linha existente.          |
| b      | Excluir linha inexistente.   |
| c      | Adicionar tabela existente.        |
| d      | Excluir tabela não existente. |
| e      | Modificar a linha existente.       |
| f      | Altere a página de código.           |



 

As condições de validação a seguir podem ser usadas para indicar quando uma transformação pode ser aplicada a um pacote. Essas condições podem ser especificadas com-g, mas não-a.



| Opção | Condição de validação                                  |
|--------|-------------------------------------------------------|
| g      | Verifique o código de atualização.                                   |
| l      | Verificar idioma.                                       |
| p      | Verifique a plataforma.                                       |
| r      | Verifique o produto.                                        |
| s      | Verifique somente a versão principal.                             |
| t      | Verifique apenas as versões principal e secundária.                  |
| u      | Verifique as versões principal, secundária e de atualização.             |
| v      | Versão do banco de dados aplicada < versão do banco de dados base.  |
| w      | Versão do banco de dados aplicada <= versão do banco de dados base. |
| x      | Versão do banco de dados aplicada = versão do banco de dados base.     |
| a      | Versão do banco de dados aplicada >= versão do banco de dados base. |
| z      | Versão do banco de dados aplicada > versão do banco de dados base.  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ferramentas de desenvolvimento Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Transformações de banco de dados](database-transforms.md)
</dt> <dt>

[Um exemplo de transformação de personalização](a-customization-transform-example.md)
</dt> <dt>

[Versões, ferramentas e redistribuíveis liberados](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



