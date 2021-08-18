---
description: A seguir estão as funções do Registro.
ms.assetid: a490b748-42e8-462b-9a7f-a8b21438ea79
title: Funções do Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81f5aff4dad00691f606911c1cf092933aa121eaf7a2d25aacbcc8a83948b89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885209"
---
# <a name="registry-functions"></a>Funções do Registro

A seguir estão as funções do Registro.



| Função                                                           | Descrição                                                                                                                                    |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSystemRegistryQuota**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)           | Recupera o tamanho atual do Registro e o tamanho máximo que o Registro tem permissão para obter no sistema.                          |
| [**Regclosekey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey)                                 | Fecha um alça para a chave do Registro especificada.                                                                                                 |
| [**RegConnectRegistry**](/windows/desktop/api/Winreg/nf-winreg-regconnectregistrya)                   | Estabelece uma conexão com um alçamento de registro predefinido em outro computador.                                                                  |
| [**RegCopyTree**](/windows/desktop/api/Winreg/nf-winreg-regcopytreea)                                 | Copia a chave do Registro especificada, juntamente com seus valores e subkeys, para a chave de destino especificada.                                        |
| [**Regcreatekeyex**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa)                           | Cria a chave do Registro especificada.                                                                                                            |
| [**RegCreateKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda)           | Cria a chave do Registro especificada e a associa a uma transação.                                                                       |
| [**RegDeleteKey**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya)                               | Exclui uma sub-chave e seus valores.                                                                                                               |
| [**RegDeleteKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeyexa)                           | Exclui uma sub-chave e seus valores da exibição específica da plataforma especificada do Registro.                                                     |
| [**RegDeleteKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeytransacteda)           | Exclui uma sub-chave e seus valores da exibição específica da plataforma especificada do Registro como uma operação transatada.                           |
| [**RegDeleteKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeyvaluea)                     | Remove o valor especificado da chave e da sub-chave do Registro especificadas.                                                                        |
| [**RegDeleteTree**](/windows/desktop/api/Winreg/nf-winreg-regdeletetreea)                             | Exclui as sub-chaves e os valores da chave especificada recursivamente.                                                                               |
| [**RegDeleteValue**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea)                           | Remove um valor nomeado da chave do Registro especificada.                                                                                         |
| [**RegDisablePredefinedCache**](/windows/desktop/api/Winreg/nf-winreg-regdisablepredefinedcache)     | Desabilita o cache de alça para o alça do Registro predefinido para **O USUÁRIO \_ ATUAL \_ do HKEY** para o processo atual.                                |
| [**RegDisablePredefinedCacheEx**](/windows/desktop/api/Winreg/nf-winreg-regdisablepredefinedcacheex) | Desabilita o cache de tratamento para todos os alças de registro predefinidos para o processo atual.                                                           |
| [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey)         | Desabilita a reflexão do Registro para a chave especificada.                                                                                            |
| [**RegEnableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey)           | Habilita a reflexão do Registro para a chave desabilitada especificada.                                                                                    |
| [**RegEnumKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa)                               | Enumera as sub-chaves da chave do Registro aberta especificada.                                                                                     |
| [**RegEnumValue**](/windows/desktop/api/Winreg/nf-winreg-regenumvaluea)                               | Enumera os valores da chave do Registro aberta especificada.                                                                                     |
| [**Regflushkey**](/windows/desktop/api/Winreg/nf-winreg-regflushkey)                                 | Grava todos os atributos da chave do Registro aberta especificada no Registro.                                                                    |
| [**RegGetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-reggetkeysecurity)                | Recupera uma cópia do descritor de segurança que protege a chave do Registro aberta especificada.                                                        |
| [**RegGetValue**](/windows/desktop/api/Winreg/nf-winreg-reggetvaluea)                                 | Recupera o tipo e os dados para o valor do Registro especificado.                                                                                  |
| [**RegLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regloadkeya)                                   | Cria uma sub-chave em **HKEY \_ USERS** ou **HKEY \_ LOCAL \_ MACHINE** e armazena informações de registro de um arquivo especificado nessa sub-chave. |
| [**RegLoadMUIString**](/windows/desktop/api/Winreg/nf-winreg-regloadmuistringa)                       | Carrega a cadeia de caracteres especificada da chave e da sub-chave especificadas.                                                                                  |
| [**RegNotifyChangeKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue)         | Notifica o chamador sobre as alterações nos atributos ou no conteúdo de uma chave do Registro especificada.                                                   |
| [**RegOpenCurrentUser**](/windows/desktop/api/Winreg/nf-winreg-regopencurrentuser)                   | Recupera um alça para a chave **DO USUÁRIO \_ ATUAL \_ do HKEY** para o usuário que o thread atual está representando.                                        |
| [**Regopenkeyex**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa)                               | Abre a chave do Registro especificada.                                                                                                              |
| [**RegOpenKeyTransacted**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda)               | Abre a chave do Registro especificada e a associa a uma transação.                                                                         |
| [**RegOpenUserClassesRoot**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot)           | Recupera um alça para a chave **\_ \_ RAIZ de CLASSES HKEY** para o usuário especificado.                                                                  |
| [**RegOverridePredefKey**](/windows/desktop/api/Winreg/nf-winreg-regoverridepredefkey)               | Mapas uma chave do Registro predefinida para uma chave do Registro especificada.                                                                                    |
| [**RegQueryInfoKey**](/windows/desktop/api/Winreg/nf-winreg-regqueryinfokeya)                         | Recupera informações sobre a chave do Registro especificada.                                                                                        |
| [**RegQueryMultipleValues**](/windows/desktop/api/Winreg/nf-winreg-regquerymultiplevaluesa)           | Recupera o tipo e os dados de uma lista de nomes de valor associados a uma chave do Registro aberta.                                                    |
| [**RegQueryReflectionKey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey)             | Determina se a reflexão foi desabilitada ou habilitada para a chave especificada.                                                              |
| [**Regqueryvalueex**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa)                         | Recupera o tipo e os dados de um nome de valor especificado associado a uma chave do Registro aberta.                                                   |
| [**Regreplacekey**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya)                             | Substitui o arquivo que está com uma chave do Registro e todas as suas sub-chaves por outro arquivo.                                                                |
| [**RegRestoreKey**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya)                             | Lê as informações do Registro em um arquivo especificado e as copia pela chave especificada.                                                       |
| [**RegSaveKey**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya)                                   | Salva a chave especificada e todas as suas sub-chaves e valores em um novo arquivo.                                                                       |
| [**RegSaveKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa)                               | Salva a chave especificada e todas as suas sub-chaves e valores em um novo arquivo. Você pode especificar o formato para a chave salva ou o hive.                 |
| [**RegSetKeyValue**](/windows/desktop/api/Winreg/nf-winreg-regsetkeyvaluea)                           | Define os dados para o valor especificado na chave e na sub-chave do Registro especificadas.                                                                |
| [**RegSetKeySecurity**](/windows/desktop/api/winreg/nf-winreg-regsetkeysecurity)                | Define a segurança de uma chave do Registro aberta.                                                                                                     |
| [**Regsetvalueex**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa)                             | Define os dados e o tipo de um valor especificado em uma chave do Registro.                                                                              |
| [**RegUnLoadKey**](/windows/desktop/api/Winreg/nf-winreg-regunloadkeya)                               | Descarrega a chave do Registro especificada e suas sub-chaves do Registro.                                                                          |



 

As seguintes funções de shell podem ser usadas com o Registro:

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

A seguir estão as funções initialization-file. Eles recuperam informações de e copiam informações para um arquivo de inicialização definido pelo sistema ou pelo aplicativo. Essas funções são fornecidas apenas para compatibilidade com versões de 16 bits do Windows. Novos aplicativos devem usar o Registro.



| Função                                                               | Descrição                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**GetPrivateProfileInt**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofileint)                   | Recupera um inteiro associado a uma chave na seção especificada de um arquivo de inicialização.     |
| [**GetPrivateProfileSection**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilesection)           | Recupera todas as chaves e valores para a seção especificada de um arquivo de inicialização.             |
| [**GetPrivateProfileSectionNames**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilesectionnames) | Recupera os nomes de todas as seções em um arquivo de inicialização.                                     |
| [**GetPrivateProfileString**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilestring)             | Recupera uma cadeia de caracteres da seção especificada em um arquivo de inicialização.                           |
| [**GetPrivateProfileStruct**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilestruct)             | Recupera os dados associados a uma chave na seção especificada de um arquivo de inicialização.       |
| [**Getprofileint**](/windows/desktop/api/Winbase/nf-winbase-getprofileinta)                                 | Recupera um inteiro de uma chave na seção especificada do arquivo Win.ini dados.                      |
| [**GetProfileSection**](/windows/desktop/api/Winbase/nf-winbase-getprofilesectiona)                         | Recupera todas as chaves e valores para a seção especificada do arquivo Win.ini dados.                   |
| [**GetProfileString**](/windows/desktop/api/Winbase/nf-winbase-getprofilestringa)                           | Recupera a cadeia de caracteres associada a uma chave na seção especificada do arquivo Win.ini dados.           |
| [**WritePrivateProfileSection**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilesectiona)       | Substitui as chaves e os valores da seção especificada em um arquivo de inicialização.                  |
| [**WritePrivateProfileString**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilestringa)         | Copia uma cadeia de caracteres na seção especificada de um arquivo de inicialização.                              |
| [**WritePrivateProfileStruct**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilestructa)         | Copia dados em uma chave na seção especificada de um arquivo de inicialização.                         |
| [**WriteProfileSection**](/windows/desktop/api/Winbase/nf-winbase-writeprofilesectiona)                     | Substitui o conteúdo da seção especificada no arquivo Win.ini chaves e valores especificados. |
| [**Writeprofilestring**](/windows/desktop/api/Winbase/nf-winbase-writeprofilestringa)                       | Copia uma cadeia de caracteres na seção especificada do arquivo Win.ini dados.                                    |



 

## <a name="obsolete-functions"></a>Funções obsoletas

Essas funções são fornecidas apenas para compatibilidade com versões de 16 bits do Windows:

-   [**RegCreateKey**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeya)
-   [**RegEnumKey**](/windows/desktop/api/Winreg/nf-winreg-regenumkeya)
-   [**Regopenkey**](/windows/desktop/api/Winreg/nf-winreg-regopenkeya)
-   [**RegQueryValue**](/windows/desktop/api/Winreg/nf-winreg-regqueryvaluea)
-   [**RegSetValue**](/windows/desktop/api/Winreg/nf-winreg-regsetvaluea)

 

 
