---
description: 'O sistema armazena informações de perfil de usuário em um diretório específico, que tem nomes diferentes em versões diferentes do Windows: &\# 0034; Documents and Settings&\# 0034; no Windows XP e &\# 0034; Os usuários&\# 0034; no Windows Vista e versões posteriores.'
title: Diretório de perfis
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 41056f40-fa1a-488a-b213-49cbdd8d4fdf
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3eb310434e5665dd8f28a661785403d72c4c1e46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968000"
---
# <a name="profiles-directory"></a>Diretório de perfis

O sistema armazena informações de perfil de usuário em um diretório específico, que tem nomes diferentes em versões diferentes do Windows: "Documents and Settings" no Windows XP e "Users" no Windows Vista e posterior. Para obter o caminho do diretório de perfis, use a função [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya) .

O diretório de perfis contém os seguintes subdiretórios para perfis de usuário.



| Diretório                                      | Descrição                                                                                                                                |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Usuários do ProgramData (Windows Vista ou posterior)/All | Informações do programa que se aplicam a todos os usuários. O diretório todos os usuários ainda existe no Windows Vista ou posterior, para compatibilidade com versões anteriores. |
| Padrão                                        | Informações de perfil que se aplicam ao usuário padrão.                                                                                      |
| *Usuário*                                         | Informações de perfil que se aplicam ao usuário especificado. Cada usuário tem seu próprio subdiretório de perfil.                                      |



 

Para obter o local do diretório ProgramData/todos os usuários, chame a função [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya) . O diretório raiz contém os seguintes subdiretórios:



| Diretório  | Descrição                          |
|------------|--------------------------------------|
| Área de trabalho    | Atalhos a serem exibidos na área de trabalho. |
| Menu Iniciar | Itens de menu para o menu **Iniciar** .   |



 

Para obter o local do diretório do usuário padrão, chame a função [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya) . Para obter o local de um determinado diretório de usuário, chame a função [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya) . O usuário padrão e os diretórios de usuário específicos contêm os seguintes subdiretórios. Os diretórios em itálico indicam os diretórios que estão ocultos por padrão. Você pode exibir esses diretórios selecionando a opção **Mostrar arquivos ocultos, pastas e unidades** no item do painel de controle de **Opções de pasta** .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Diretório</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Dados de aplicativos</td>
<td>Dados específicos do aplicativo.</td>
</tr>
<tr class="even">
<td>Cookies</td>
<td>Cookies do Windows Internet Explorer.</td>
</tr>
<tr class="odd">
<td>Área de trabalho</td>
<td>Atalhos a serem exibidos na área de trabalho.</td>
</tr>
<tr class="even">
<td>Favoritos</td>
<td>Links para sites favoritos.</td>
</tr>
<tr class="odd">
<td>Configurações locais</td>
<td>Configurações de aplicativo e dados que não são movidos com o perfil. Normalmente, as configurações ou os dados nesse diretório são específicos do computador ou são muito grandes para serem movidos com eficiência. Esse diretório contém as seguintes subpastas:
<ul>
<li>Dados de aplicativos</li>
<li>Histórico</li>
<li>Temp</li>
<li>Arquivos Temporários da Internet</li>
</ul></td>
</tr>
<tr class="even">
<td>Meus Documentos</td>
<td>O local padrão para documentos que o usuário cria. Por padrão, os aplicativos devem salvar arquivos de documento nesse diretório.</td>
</tr>
<tr class="odd">
<td><em>NetHood</em></td>
<td>Atalhos para itens de ambiente de rede.</td>
</tr>
<tr class="even">
<td><em>PrintHood</em></td>
<td>Atalhos para itens de pasta da impressora.</td>
</tr>
<tr class="odd">
<td><em>Recente</em></td>
<td>Atalhos para os documentos usados mais recentemente.</td>
</tr>
<tr class="even">
<td>SendTo</td>
<td>Atalhos para locais nos quais o usuário geralmente envia arquivos.</td>
</tr>
<tr class="odd">
<td>Menu Iniciar</td>
<td>Itens de menu para o menu <strong>Iniciar</strong> .</td>
</tr>
<tr class="even">
<td><em>Modelos</em></td>
<td>Atalhos para itens de modelo.</td>
</tr>
</tbody>
</table>



 

Para obter o local de subdiretórios desses diretórios, use as funções [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) ou [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) .

 

 



