---
description: Esta seção descreve as funções de manipulação de registro do shell do Windows. Os elementos de programação explicados nesta documentação são exportados por Shlwapi.dll e definidos em Shlwapi. h e shlwapi. lib.
title: Funções de manipulação de registro do Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 12182f56-5bb3-4f70-ae6a-2ef7366287b9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8a3e4f65904fa97635b3ef4dc3abd9f01344f6a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989080"
---
# <a name="shell-registry-handling-functions"></a>Funções de manipulação de registro do Shell

Esta seção descreve as funções de manipulação de registro do shell do Windows. Os elementos de programação explicados nesta documentação são exportados por Shlwapi.dll e definidos em Shlwapi. h e shlwapi. lib.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                             | Descrição                                                                                                                                                                         |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AssocCreate**](/windows/desktop/api/Shlwapi/nf-shlwapi-assoccreate)<br/>                     | Retorna um ponteiro para um objeto [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .<br/>                                                                                         |
| [**AssocGetPerceivedType**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocgetperceivedtype)<br/> | Recupera o tipo percebido de um arquivo com base em sua extensão.<br/>                                                                                                                |
| [**AssocIsDangerous**](/windows/desktop/api/Shlwapi/nf-shlwapi-associsdangerous)<br/>           | Determina se um tipo de arquivo é considerado um risco de segurança em potencial.<br/>                                                                                                  |
| [**AssocQueryKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerykeya)<br/>                 | Pesquisa e recupera uma chave relacionada a uma associação de arquivo ou protocolo do registro.<br/>                                                                            |
| [**AssocQueryString**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringa)<br/>           | Pesquisa e recupera uma cadeia de caracteres relacionada a associação de arquivo ou protocolo do registro.<br/>                                                                              |
| [**AssocQueryStringByKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-assocquerystringbykeya)<br/> | Pesquisa e recupera uma cadeia de caracteres relacionada à associação de arquivo do registro a partir de uma chave especificada.<br/>                                                            |
| [**SHCopyKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcopykeya)<br/>                         | Copia recursivamente as sub-chaves e os valores da subchave de origem para a chave de destino. [**SHCopyKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shcopykeya) não copia os atributos de segurança das chaves.<br/> |
| [**SHDeleteEmptyKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeleteemptykeya)<br/>           | Exclui uma chave vazia.<br/>                                                                                                                                                    |
| [**SHDeleteKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeletekeya)<br/>                     | Exclui uma subchave e todos os seus descendentes. Essa função remove a chave e todos os valores da chave do registro.<br/>                                                      |
| [**SHDeleteValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shdeletevaluea)<br/>                 | Exclui um valor nomeado da chave do Registro especificada.<br/>                                                                                                                   |
| [**SHEnumKeyEx**](/windows/desktop/api/Shlwapi/nf-shlwapi-shenumkeyexa)<br/>                     | Enumera as subchaves da chave do registro aberta especificada.<br/>                                                                                                               |
| [**SHEnumValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shenumvaluea)<br/>                     | Enumera os valores da chave de registro aberta especificada.<br/>                                                                                                                |
| [**SHGetAssocKeys**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetassockeys)<br/>               | Recupera uma matriz de subchaves de classe associadas a um objeto [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .<br/>                                                          |
| [**SHGetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shgetvaluea)<br/>                       | Recupera um valor de registro.<br/>                                                                                                                                              |
| [**SHOpenRegStream2**](/windows/desktop/api/Shlwapi/nf-shlwapi-shopenregstream2a)<br/>           | Abre um valor de registro e fornece um fluxo que pode ser usado para ler ou gravar no valor. Essa função substitui [**SHOpenRegStream**](/windows/desktop/api/Shlwapi/nf-shlwapi-shopenregstreama).<br/>   |
| [**SHQueryInfoKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shqueryinfokeya)<br/>               | Recupera informações sobre uma chave do Registro especificada.<br/>                                                                                                                    |
| [**SHQueryValueEx**](/windows/desktop/api/Shlwapi/nf-shlwapi-shqueryvalueexa)<br/>               | Abre uma chave do registro e a consulta para um valor específico.<br/>                                                                                                                |
| [**SHRegCloseUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregcloseuskey)<br/>             | Fecha um identificador para uma subchave do Registro específica do usuário em uma subárvore específica do usuário (HKEY \_ Current \_ User ou HKEY \_ local \_ Machine).<br/>                                             |
| [**SHRegCreateUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregcreateuskeya)<br/>           | Cria ou abre uma subchave do registro em uma subárvore específica do usuário (HKEY \_ Current \_ User ou HKEY \_ local \_ Machine).<br/>                                                             |
| [**SHRegDeleteEmptyUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregdeleteemptyuskeya)<br/> | Exclui uma subchave do registro vazia em uma subárvore específica do usuário (HKEY \_ Current \_ User ou HKEY \_ local \_ Machine).<br/>                                                               |
| [**SHRegDeleteUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregdeleteusvaluea)<br/>       | Exclui um valor de subchave do registro em uma subárvore específica do usuário (HKEY \_ Current \_ User ou HKEY \_ local \_ Machine).<br/>                                                                |
| [**SHRegDuplicateHKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregduplicatehkey)<br/>       | Duplica o identificador HKEY de uma chave do registro.<br/>                                                                                                                                 |
| [**SHRegEnumUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregenumuskeya)<br/>               | Enumera as sub-chaves de uma subchave do registro em uma subárvore específica do usuário (HKEY \_ Current \_ User ou HKEY \_ local \_ Machine).<br/>                                                    |
| [**SHRegEnumUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregenumusvaluea)<br/>           | Enumera os valores da subchave do Registro especificada em uma subárvore específica do usuário (HKEY \_ Current \_ User ou HKEY \_ local \_ Machine).<br/>                                         |
| [**SHRegGetBoolUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetboolusvaluea)<br/>     | Recupera um valor booliano de uma subchave do registro em uma subárvore específica do usuário (HKEY \_ Current \_ User ou HKEY \_ local \_ Machine).<br/>                                               |
| [**SHRegGetIntW**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetintw)<br/>                    | Lê um valor numérico de cadeia de caracteres do registro e converte-o em um inteiro.<br/>                                                                                            |
| [**SHRegGetPath**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetpatha)<br/>                   | Recupera um caminho de arquivo do registro, expandindo variáveis de ambiente conforme necessário.<br/>                                                                                      |
| [**SHRegGetUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shreggetusvaluea)<br/>             | Recupera um valor de uma subchave do registro em uma subárvore específica do usuário (HKEY \_ Current \_ User ou HKEY \_ local \_ Machine).<br/>                                                       |
| [**SHRegOpenUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregopenuskeya)<br/>               | Abre uma subchave do registro em uma subárvore específica do usuário (HKEY \_ Current \_ User ou HKEY \_ local \_ Machine).<br/>                                                                        |
| [**SHRegQueryInfoUSKey**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregqueryinfouskeya)<br/>     | Recupera informações sobre uma subchave do Registro especificada em uma subárvore específica do usuário (HKEY \_ Current \_ User ou HKEY \_ local \_ Machine).<br/>                                        |
| [**SHRegQueryUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregqueryusvaluea)<br/>         | Recupera o tipo e os dados para um nome especificado associado a uma subchave do registro aberto em uma subárvore específica do usuário (HKEY \_ Current \_ User ou HKEY \_ local \_ Machine).<br/>       |
| [**SHRegSetPath**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregsetpatha)<br/>                   | Usa um caminho de arquivo, substitui nomes de pastas por cadeias de caracteres de ambiente e coloca a cadeia de caracteres resultante no registro.<br/>                                                      |
| [**SHRegSetUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregsetusvaluea)<br/>             | Define um valor de subchave do registro em uma subárvore específica do usuário (HKEY \_ Current \_ User ou HKEY \_ local \_ Machine).<br/>                                                                   |
| [**SHRegSetValue**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetvalue)<br/>                 | Define um valor de registro.<br/> Use [**RegSetValue**](/windows/win32/api/winreg/nf-winreg-regsetvaluea) em seu lugar.<br/>                                                                                  |
| [**SHRegWriteUSValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shregwriteusvaluea)<br/>         | Grava um valor em uma subchave do registro em uma subárvore específica do usuário (HKEY \_ Current \_ User ou HKEY \_ local \_ Machine).<br/>                                                            |
| [**SHSetValue**](/windows/desktop/api/Shlwapi/nf-shlwapi-shsetvaluea)<br/>                       | Define o valor de uma chave do registro.<br/>                                                                                                                                        |



 

 

 
