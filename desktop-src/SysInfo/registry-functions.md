---
description: A seguir estão as funções de registro.
ms.assetid: a490b748-42e8-462b-9a7f-a8b21438ea79
title: Funções de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc2cfadd3753b7a269667fee22955f8465495458
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169822"
---
# <a name="registry-functions"></a>Funções de registro

A seguir estão as funções de registro.



| Função                                                           | Descrição                                                                                                                                    |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)           | Recupera o tamanho atual do registro e o tamanho máximo que o registro tem permissão para alcançar no sistema.                          |
| [**Falha RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey)                                 | Fecha um identificador para a chave do Registro especificada.                                                                                                 |
| [**RegConnectRegistry**](/windows/desktop/api/Winreg/nf-winreg-regconnectregistrya)                   | Estabelece uma conexão com um identificador de registro predefinido em outro computador.                                                                  |
| [**RegCopyTree**](/windows/desktop/api/Winreg/nf-winreg-regcopytreea)                                 | Copia a chave do Registro especificada, juntamente com seus valores e subchaves, para a chave de destino especificada.                                        |
| [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa)                           | Cria a chave do Registro especificada.                                                                                                            |
| [**RegCreateKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda)           | Cria a chave do Registro especificada e a associa a uma transação.                                                                       |
| [**RegDeleteKey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya)                               | Exclui uma subchave e seus valores.                                                                                                               |
| [**RegDeleteKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeyexa)                           | Exclui uma subchave e seus valores da exibição específica da plataforma especificada do registro.                                                     |
| [**RegDeleteKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeytransacteda)           | Exclui uma subchave e seus valores da exibição específica da plataforma especificada do registro como uma operação transacionada.                           |
| [**RegDeleteKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeyvaluea)                     | Remove o valor especificado da chave e da subchave do registro especificado.                                                                        |
| [**RegDeleteTree**](/windows/desktop/api/Winreg/nf-winreg-regdeletetreea)                             | Exclui as subchaves e valores da chave especificada recursivamente.                                                                               |
| [**Falha em RegDeleteValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea)                           | Remove um valor nomeado da chave do Registro especificada.                                                                                         |
| [**RegDisablePredefinedCache**](/windows/desktop/api/Winreg/nf-winreg-regdisablepredefinedcache)     | Desabilita o cache de identificadores para o identificador de registro predefinido para **HKEY \_ Current \_ User** para o processo atual.                                |
| [**RegDisablePredefinedCacheEx**](/windows/desktop/api/Winreg/nf-winreg-regdisablepredefinedcacheex) | Desabilita o cache de identificadores para todos os identificadores de registro predefinidos para o processo atual.                                                           |
| [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey)         | Desabilita a reflexão do registro para a chave especificada.                                                                                            |
| [**RegEnableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey)           | Habilita a reflexão do registro para a chave desabilitada especificada.                                                                                    |
| [**RegEnumKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa)                               | Enumera as subchaves da chave do registro aberta especificada.                                                                                     |
| [**RegEnumValue**](/windows/desktop/api/Winreg/nf-winreg-regenumvaluea)                               | Enumera os valores para a chave de registro aberta especificada.                                                                                     |
| [**RegFlushKey**](/windows/desktop/api/Winreg/nf-winreg-regflushkey)                                 | Grava todos os atributos da chave do registro aberta especificada no registro.                                                                    |
| [**RegGetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-reggetkeysecurity)                | Recupera uma cópia do descritor de segurança protegendo a chave de registro aberta especificada.                                                        |
| [**RegGetValue**](/windows/desktop/api/Winreg/nf-winreg-reggetvaluea)                                 | Recupera o tipo e os dados para o valor do registro especificado.                                                                                  |
| [**RegLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regloadkeya)                                   | Cria uma subchave em **HKEY \_ Users** ou **HKEY \_ local \_ Machine** e armazena informações de registro de um arquivo especificado nessa subchave. |
| [**RegLoadMUIString**](/windows/desktop/api/Winreg/nf-winreg-regloadmuistringa)                       | Carrega a cadeia de caracteres especificada da chave e da subchave especificada.                                                                                  |
| [**RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue)         | Notifica o chamador sobre as alterações nos atributos ou no conteúdo de uma chave do Registro especificada.                                                   |
| [**RegOpenCurrentUser**](/windows/desktop/api/Winreg/nf-winreg-regopencurrentuser)                   | Recupera um identificador para a chave de **\_ \_ usuário atual de hKey** para o usuário que o thread atual está representando.                                        |
| [**Falha em RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa)                               | Abre a chave do Registro especificada.                                                                                                              |
| [**RegOpenKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda)               | Abre a chave do Registro especificada e a associa a uma transação.                                                                         |
| [**RegOpenUserClassesRoot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot)           | Recupera um identificador para a chave de **\_ \_ raiz de classes hKey** para o usuário especificado.                                                                  |
| [**RegOverridePredefKey**](/windows/desktop/api/Winreg/nf-winreg-regoverridepredefkey)               | Mapeia uma chave do registro predefinida para uma chave do Registro especificada.                                                                                    |
| [**RegQueryInfoKey**](/windows/desktop/api/Winreg/nf-winreg-regqueryinfokeya)                         | Recupera informações sobre a chave do Registro especificada.                                                                                        |
| [**RegQueryMultipleValues**](/windows/desktop/api/Winreg/nf-winreg-regquerymultiplevaluesa)           | Recupera o tipo e os dados para uma lista de nomes de valores associados a uma chave de registro aberta.                                                    |
| [**RegQueryReflectionKey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey)             | Determina se a reflexão foi desabilitada ou habilitada para a chave especificada.                                                              |
| [**RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa)                         | Recupera o tipo e os dados para um nome de valor especificado associado a uma chave de registro aberta.                                                   |
| [**RegReplaceKey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya)                             | Substitui o arquivo de backup de uma chave do registro e de todas as suas subchaves por outro arquivo.                                                                |
| [**RegRestoreKey**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya)                             | Lê as informações de registro em um arquivo especificado e as copia sobre a chave especificada.                                                       |
| [**RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya)                                   | Salva a chave especificada e todas as suas subchaves e valores em um novo arquivo.                                                                       |
| [**RegSaveKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa)                               | Salva a chave especificada e todas as suas subchaves e valores em um novo arquivo. Você pode especificar o formato para a chave ou o hive salvo.                 |
| [**RegSetKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regsetkeyvaluea)                           | Define os dados para o valor especificado na chave do registro e na subchave especificada.                                                                |
| [**RegSetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-regsetkeysecurity)                | Define a segurança de uma chave de registro aberta.                                                                                                     |
| [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa)                             | Define os dados e o tipo de um valor especificado em uma chave do registro.                                                                              |
| [**RegUnLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regunloadkeya)                               | Descarrega a chave do Registro especificada e suas subchaves do registro.                                                                          |



 

As seguintes funções de shell podem ser usadas com o registro:

-   [**AssocCreate**](/windows/desktop/api/shlwapi/nf-shlwapi-assoccreate)
-   [**AssocQueryKey**](/windows/desktop/api/shlwapi/nf-shlwapi-assocquerykeya)
-   [**AssocQueryString**](/windows/desktop/api/shlwapi/nf-shlwapi-assocquerystringa)
-   [**AssocQueryStringByKey**](/windows/desktop/api/shlwapi/nf-shlwapi-assocquerystringbykeya)
-   [**SHCopyKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shcopykeya)
-   [**SHDeleteEmptyKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shdeleteemptykeya)
-   [**SHDeleteKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shdeletekeya)
-   [**SHDeleteValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shdeletevaluea)
-   [**SHEnumKeyEx**](/windows/desktop/api/shlwapi/nf-shlwapi-shenumkeyexa)
-   [**SHEnumValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shenumvaluea)
-   [**SHGetValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shgetvaluea)
-   [**SHQueryInfoKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shqueryinfokeya)
-   [**SHQueryValueEx**](/windows/desktop/api/shlwapi/nf-shlwapi-shqueryvalueexa)
-   [**SHRegCloseUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregcloseuskey)
-   [**SHRegCreateUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregcreateuskeya)
-   [**SHRegDeleteEmptyUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregdeleteemptyuskeya)
-   [**SHRegDeleteUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregdeleteusvaluea)
-   [**SHRegDuplicateHKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregduplicatehkey)
-   [**SHRegEnumUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregenumuskeya)
-   [**SHRegEnumUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregenumusvaluea)
-   [**SHRegGetBoolUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetboolusvaluea)
-   [**SHRegGetIntW**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetintw)
-   [**SHRegGetPath**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetpatha)
-   [**SHRegGetUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetusvaluea)
-   [**SHRegOpenUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregopenuskeya)
-   [**SHRegQueryInfoUSKey**](/windows/desktop/api/shlwapi/nf-shlwapi-shregqueryinfouskeya)
-   [**SHRegQueryUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregqueryusvaluea)
-   [**SHRegSetPath**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetpatha)
-   [**SHRegSetUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetusvaluea)
-   [**SHRegWriteUSValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregwriteusvaluea)
-   [**SHSetValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shsetvaluea)

A seguir estão as funções de arquivo de inicialização. Eles recuperam informações de e copiam informações para um arquivo de inicialização definido pelo sistema ou pelo aplicativo. Essas funções são fornecidas apenas para compatibilidade com versões de 16 bits do Windows. Os novos aplicativos devem usar o registro.



| Função                                                               | Descrição                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**GetPrivateProfileInt**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofileint)                   | Recupera um inteiro associado a uma chave na seção especificada de um arquivo de inicialização.     |
| [**GetPrivateProfileSection**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilesection)           | Recupera todas as chaves e valores para a seção especificada de um arquivo de inicialização.             |
| [**GetPrivateProfileSectionNames**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilesectionnames) | Recupera os nomes de todas as seções em um arquivo de inicialização.                                     |
| [**GetPrivateProfileString**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilestring)             | Recupera uma cadeia de caracteres da seção especificada em um arquivo de inicialização.                           |
| [**GetPrivateProfileStruct**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilestruct)             | Recupera os dados associados a uma chave na seção especificada de um arquivo de inicialização.       |
| [**GetProfileInt**](/windows/desktop/api/Winbase/nf-winbase-getprofileinta)                                 | Recupera um inteiro de uma chave na seção especificada do arquivo de Win.ini.                      |
| [**GetProfileSection**](/windows/desktop/api/Winbase/nf-winbase-getprofilesectiona)                         | Recupera todas as chaves e valores da seção especificada do arquivo de Win.ini.                   |
| [**GetProfileString**](/windows/desktop/api/Winbase/nf-winbase-getprofilestringa)                           | Recupera a cadeia de caracteres associada a uma chave na seção especificada do arquivo de Win.ini.           |
| [**WritePrivateProfileSection**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilesectiona)       | Substitui as chaves e valores da seção especificada em um arquivo de inicialização.                  |
| [**WritePrivateProfileString**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilestringa)         | Copia uma cadeia de caracteres na seção especificada de um arquivo de inicialização.                              |
| [**WritePrivateProfileStruct**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilestructa)         | Copia dados em uma chave na seção especificada de um arquivo de inicialização.                         |
| [**WriteProfileSection**](/windows/desktop/api/Winbase/nf-winbase-writeprofilesectiona)                     | Substitui o conteúdo da seção especificada no arquivo Win.ini com chaves e valores especificados. |
| [**WriteProfileString**](/windows/desktop/api/Winbase/nf-winbase-writeprofilestringa)                       | Copia uma cadeia de caracteres na seção especificada do arquivo de Win.ini.                                    |



 

## <a name="obsolete-functions"></a>Funções obsoletas

Essas funções são fornecidas apenas para compatibilidade com versões de 16 bits do Windows:

-   [**RegCreateKey**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeya)
-   [**RegEnumKey**](/windows/desktop/api/Winreg/nf-winreg-regenumkeya)
-   [**RegOpenKey**](/windows/desktop/api/Winreg/nf-winreg-regopenkeya)
-   [**RegQueryValue**](/windows/desktop/api/Winreg/nf-winreg-regqueryvaluea)
-   [**RegSetValue**](/windows/desktop/api/Winreg/nf-winreg-regsetvaluea)

 

 
