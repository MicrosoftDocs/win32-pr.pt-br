---
description: o arquivo VBScript WiSumInf.vbs é fornecido nos componentes SDK do Windows para os desenvolvedores de Windows Installer. este script de exemplo pode ser usado para gerenciar o fluxo de informações de resumo de um pacote de Windows Installer.
ms.assetid: f7f1cf89-f211-4511-8260-b48c898c1cf6
title: Gerenciar informações de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bf5ad72ee4f308831077ec2f732b92a70f407c560b204d10f2d3db63d1bb9bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926966"
---
# <a name="manage-summary-information"></a>Gerenciar informações de resumo

o arquivo VBScript WiSumInf.vbs é fornecido nos [componentes SDK do Windows para os desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md). este script de exemplo pode ser usado para gerenciar o [fluxo de informações de resumo](summary-information-stream.md) de um pacote de Windows Installer.

O exemplo demonstra o uso de:

-   [**Propriedade SummaryInformation (objeto do instalador)**](installer-summaryinformation.md)
-   [**Método LastErrorRecord**](installer-lasterrorrecord.md) do [ **objeto do instalador**](installer-object.md)

o uso deste exemplo requer a versão CScript.exe ou WScript.exe do Host de Script Windows. Para usar CScript.exe para executar este exemplo, digite um comando no prompt de comando usando a sintaxe a seguir. A ajuda será exibida se o primeiro argumento for/? ou se poucos argumentos forem especificados. Para redirecionar a saída para um arquivo, termine a linha de comando com VBS > \[ *caminho para o arquivo* \] . O exemplo retorna um valor de 0 para êxito, 1 se a ajuda for invocada e 2 se o script falhar.

**cscript WiSumInf.vbs \[ caminho para a propriedade do banco de dados \] \[ = valor\]**

especifique o caminho para o banco de dados de Windows Installer. Se nenhum outro argumento for especificado, o script listará todas as propriedades de resumo do pacote. Especifique uma lista de propriedades e valores de resumo a serem atualizados usando o formato Property = Value. Você pode especificar a propriedade pelo nome ou valor de PID mostrado abaixo. Os campos de data e hora usam o formato de localidade atual ou "Now" ou "Date". Para obter mais informações, consulte [Summary Information Stream Property Set](summary-information-stream-property-set.md).



| PID | Nome        | Descrição                                                                                                                                                                                                                                                                                      |
|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1   | codepage    | Página de código ANSI de cadeias de caracteres de texto em informações de resumo. Para obter mais informações, consulte [**CodePage Summary**](codepage-summary.md) Property.                                                                                                                                                           |
| 2   | Título       | tipo de pacote de Windows Installer. Para obter mais informações, consulte [**título Summary Property**](title-summary.md).                                                                                                                                                                                    |
| 3   | Assunto     | Nome completo do produto. Para obter mais informações, consulte [**propriedade de resumo do assunto**](subject-summary.md).                                                                                                                                                                                               |
| 4   | Autor      | Criador, normalmente o nome do fornecedor. Para obter mais informações, consulte [**propriedade de resumo do autor**](author-summary.md).                                                                                                                                                                                     |
| 5   | Palavras-chave    | Lista de palavras-chave para uso pelo navegador de arquivos. Para obter mais informações, consulte [**propriedade de Resumo de palavras-chave**](keywords-summary.md).                                                                                                                                                                       |
| 6   | Comentários    | Descrição da finalidade ou uso do pacote. Para obter mais informações, consulte [**comentários Summary Property**](comments-summary.md).                                                                                                                                                                       |
| 7   | Modelo    | Plataformas e idiomas com suporte. Para obter mais informações, consulte [**propriedade de resumo do modelo**](template-summary.md).                                                                                                                                                                              |
| 8   | LastAuthor  | Defina somente pelo instalador. Para obter mais informações, consulte [**última gravação por propriedade de resumo**](last-saved-by-summary.md).                                                                                                                                                                            |
| 9   | Revisão    | GUID de código do pacote. Para obter mais informações, consulte [**propriedade de resumo do número de revisão**](revision-number-summary.md).                                                                                                                                                                                |
| 11  | Exibido     | Data e hora da imagem de instalação. Para obter mais informações, consulte [**última Propriedade Resumo impressa**](last-printed-summary.md).                                                                                                                                                                    |
| 12  | Criado     | Data e hora da criação do pacote. Para obter mais informações, consulte [**criar propriedade de Resumo de data/hora**](create-time-date-summary.md).                                                                                                                                                              |
| 13  | Salvo       | Data e hora da última modificação do pacote. Para obter mais informações, consulte [**última propriedade de Resumo de data/hora salva**](last-saved-time-date-summary.md).                                                                                                                                             |
| 14  | Pages (Páginas)       | versão mínima do Windows Installer necessária para este pacote. Para obter mais informações, consulte [**propriedade de Resumo de contagem de página**](page-count-summary.md).                                                                                                                                             |
| 15  | Palavra       | Tipo de imagem do arquivo de origem. Para obter mais informações, consulte [**propriedade de Resumo de contagem de palavras**](word-count-summary.md). a partir do Windows Installer versão 4,0 no Windows Vista e no Windows Server 2008, essa propriedade inclui bits para especificar se são necessários privilégios elevados.<br/> |
| 16  | Characters  | Usado somente para transformações. [**Contagem de caracteres**](character-count-summary.md).                                                                                                                                                                                                                    |
| 18  | Aplicativo | aplicativo associado a este arquivo, ou seja, "Windows Installer". Para obter mais informações, consulte [**criando a propriedade de resumo do aplicativo**](creating-application-summary.md).                                                                                                                        |
| 19  | Segurança    | Configuração de segurança. Para obter mais informações, consulte [**Security Summary Property**](security-summary.md).                                                                                                                                                                                               |



 

para obter exemplos de script adicionais, consulte [Windows Installer exemplos de script](windows-installer-scripting-examples.md). para utilitários de exemplo que não exigem Windows Host de Script, consulte [Windows Installer ferramentas de desenvolvimento](windows-installer-development-tools.md).

 

 




