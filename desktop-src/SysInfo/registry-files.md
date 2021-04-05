---
description: Os aplicativos podem salvar parte do registro em um arquivo e, em seguida, carregar o conteúdo do arquivo de volta para o registro.
ms.assetid: a71a564d-934a-46e8-b555-989a6fa82337
title: Arquivos do registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44916618946f6541495186aa5843799c9b864fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921896"
---
# <a name="registry-files"></a>Arquivos do registro

Os aplicativos podem salvar parte do registro em um arquivo e, em seguida, carregar o conteúdo do arquivo de volta para o registro. Um arquivo de registro é útil quando uma grande quantidade de dados está sendo manipulada, quando muitas entradas estão sendo feitas no registro ou quando os dados são transitórios e devem ser carregados e descarregados novamente. Os aplicativos que fazem backup e restauram partes do registro provavelmente usarão arquivos de registro.

Para salvar uma chave e suas subchaves e valores em um arquivo de registro, um aplicativo pode chamar a função [**RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) ou [**RegSaveKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) .

[**RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) e [**RegSaveKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) crie o arquivo com o atributo Archive. O arquivo é criado no diretório atual do processo para uma chave local e no diretório% systemroot% \\ System32 para uma chave remota.

Os arquivos do registro têm os dois formatos a seguir: Standard e mais recente. O formato padrão é o único formato suportado pelo Windows 2000. Ele também é compatível com versões posteriores do Windows para compatibilidade com versões anteriores. [**RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya) cria arquivos no formato padrão.

O formato mais recente tem suporte a partir do Windows XP. Os arquivos do registro criados neste formato não podem ser carregados no Windows 2000. O [**RegSaveKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa) pode salvar arquivos do registro em qualquer formato especificando o \_ formato padrão do reg ou o \_ \_ formato reg mais recente \_ . Portanto, ele pode ser usado para converter arquivos do registro que usam o formato padrão para o formato mais recente.

Para gravar o arquivo de registro de volta no registro, um aplicativo pode usar as funções [**RegLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regloadkeya), [**RegReplaceKey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya)ou [**RegRestoreKey**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya) da seguinte maneira.

-   **RegLoadKey** carrega dados de registro de um arquivo especificado em uma subchave especificada em **HKEY \_ Users** ou **HKEY \_ local \_ Machine** no computador do aplicativo de chamada ou em um computador remoto. A função criará a subchave especificada se ela ainda não existir. Depois de chamar essa função, um aplicativo pode usar a função [**RegUnLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regunloadkeya) para restaurar o registro para seu estado anterior.
-   [**RegReplaceKey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya) substitui uma chave e todas as suas subchaves e valores no registro pelos dados contidos em um arquivo especificado. Os novos dados entrarão em vigor na próxima vez em que o sistema for iniciado.
-   [**RegRestoreKey**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya) carrega dados do registro de um arquivo especificado em uma chave especificada no computador do aplicativo de chamada ou em um computador remoto. Essa função substitui as subchaves e valores abaixo da chave especificada pelas subchaves e valores que seguem a chave de nível superior no arquivo.

A função [**RegConnectRegistry**](/windows/desktop/api/Winreg/nf-winreg-regconnectregistrya) estabelece uma conexão com um identificador de registro predefinido em outro computador. Um aplicativo usa essa função principalmente para acessar informações de um registro remoto em outros computadores em um ambiente de rede, o que você também pode fazer usando o editor do registro. Talvez você queira acessar um registro remoto para fazer backup de um registro ou controlar o acesso à rede a ele. Observe que você deve ter as permissões apropriadas para acessar um registro remoto usando essa função.

 

 



