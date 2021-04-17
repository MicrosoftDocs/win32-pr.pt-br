---
description: Msistuff.exe é um utilitário de linha de comando que pode ser usado para exibir ou configurar os recursos no executável de inicialização Setup.exe.
ms.assetid: df79574c-d0e7-45e3-97c1-d62f700260ce
title: Msistuff.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b56d6b183128971501fd3ad8ddb7a88d08cee70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811836"
---
# <a name="msistuffexe"></a>Msistuff.exe

Msistuff.exe é um utilitário de linha de comando que pode ser usado para exibir ou configurar os recursos no executável de inicialização Setup.exe.

Essa ferramenta só está disponível nos [componentes SDK do Windows para desenvolvedores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="syntax"></a>Syntax

**msistuff setup.exe** *opção {Value}*

Se nenhum dado for especificado após uma opção, esse recurso será removido.

## <a name="command-line-options"></a>Opções de linha de comando

Msistuff.exe usa as seguintes opções de linha de comando que não diferenciam maiúsculas de minúsculas. Um delimitador de barra também pode ser usado no lugar de um traço. Se uma opção for listada várias vezes, apenas a última ocorrência será usada.



| Opção               | ID de Recurso                  | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nenhuma opção especificada |                              | Exibir recursos configuráveis no Setup.exe.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **-u**               | ISETUPPROPNAME \_ BASEURL      | Set BaseURL, o local da URL base de Setup.exe. Se nenhum valor estiver presente, o local do Setup.exe será padronizado para mídia removível. Somente instalações baseadas em URL estão sujeitas a uma verificação com [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust). A barra à direita na URL é opcional. Essa opção pode ser omitida.                                                                                                                                                                                                                     |
| **-d**               | \_banco de dados ISETUPPROPNAME     | Defina msi, o nome do arquivo. msi. Esse é um caminho relativo para o arquivo. msi em relação ao local do programa de Setup.exe. Essa opção será necessária se a opção-m não for especificada. As opções-d e-m são mutuamente exclusivas. Eles não podem ser ambos especificados.                                                                                                                                                                                                                                                    |
| **-m**               | PATCH do ISETUPPROPNAME \_        | Defina msp, o nome do arquivo. msp. Este é um caminho relativo para o arquivo. msp em relação ao local do programa de Setup.exe. Essa opção será necessária se a opção-d não for especificada. As opções-m e-d são mutuamente exclusivas. Eles não podem ser ambos especificados.                                                                                                                                                                                                                                                    |
| **-n**               | ISETUPPROPNAME \_ NomeDoProduto  | Defina nome do produto, o nome do produto. Isso fornece o nome usado no texto da faixa para a interface do usuário baixada. Essa opção pode ser omitida. Se for omitido, o padrão será "The Product".                                                                                                                                                                                                                                                                                                                            |
| **-o**               | \_operação ISETUPPROPNAME    | Especifique o tipo de operação a ser executada. Os valores válidos são INSTALL, MINPATCH, MAJPATCH e INSTALLUPD. Para obter informações adicionais sobre essas opções, consulte [inicialização de download da Internet](internet-download-bootstrapping.md).                                                                                                                                                                                                                                                                                           |
| **-v**               | \_MSI mínimo de ISETUPPROPNAME \_ | Defina a versão mínima do MSI, a versão mínima do Windows Installer necessária no computador. Se a versão mínima do Windows Installer não estiver presente no computador, o [Instmsi.exe](instmsi-exe.md) apropriado será instalado para atualizar o Windows Installer. O valor dessa propriedade tem o mesmo formato que o valor PID \_ PageCount. Consulte Propriedade de [**Resumo de contagem de página**](page-count-summary.md) . O valor deve ser pelo menos 200, o valor para a Windows Installer versão 2,0. Essa opção é obrigatória. |
| **-i**               | ISETUPPROPNAME \_ INSTLOCATION | Defina o local de URL de InstMsi, o local da URL base dos executáveis de atualização Windows Installer. Se esse valor estiver ausente, o local dos executáveis de atualização será padronizado para o local de Setup.exe. Essa opção pode ser omitida.                                                                                                                                                                                                                                                                                                |
| **-a**               | ISETUPPROPNAME \_ INSTMSIA     | Defina InstMsiA, o nome da versão ANSI do executável de atualização Windows Installer. Este é um caminho relativo para a versão ANSI do Instmsi.exe em relação ao local especificado por ISETUPPROPNAME \_ INSTLOCATION. Essa opção é obrigatória.                                                                                                                                                                                                                                                                                   |
| **-w**               | ISETUPPROPNAME \_ INSTMSIW     | Defina InstMsiW, o nome da versão Unicode do executável de atualização do Windows Installer. Este é um caminho relativo para a versão Unicode do Instmsi.exe em relação ao local especificado por ISETUPPROPNAME \_ INSTLOCATION. Essa opção é obrigatória.                                                                                                                                                                                                                                                                             |
| **-p**               | Propriedades de ISETUPPROPNAME \_   | Defina as cadeias de caracteres PROPERTY = VALUE. Esses são os pares PROPERTY = VALUE a serem incluídos na linha de comando. Essa opção pode ser omitida. Essa opção não pode ser listada várias vezes e deve ser listada por último na linha de comando. Toda a linha de comando após-p é considerada como uma parte do {Value}.                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Ferramentas de desenvolvimento Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Inicialização de download da Internet](internet-download-bootstrapping.md)
</dt> <dt>

[Um exemplo de instalação com base em URL Windows Installer](a-url-based-windows-installer-installation-example.md)
</dt> <dt>

[Versões, ferramentas e redistribuíveis liberados](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 
