---
description: Este tópico discute as instruções de programação para localizar cadeias de caracteres de registro redirecionadas. Para obter mais informações, consulte usando o redirecionamento de cadeia de caracteres do registro.
ms.assetid: 03d1512f-35a6-4b3a-9a0e-97e17bd9b126
title: Localizando cadeias de caracteres redirecionadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f11600ad57c04de54d914c2c876b67967dfa1467
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757832"
---
# <a name="locating-redirected-strings"></a>Localizando cadeias de caracteres redirecionadas

Este tópico discute as instruções de programação para localizar cadeias de caracteres de registro redirecionadas. Para obter mais informações, consulte [usando o redirecionamento de cadeia de caracteres do registro](using-registry-string-redirection.md).

## <a name="load-a-language-neutral-registry-value"></a>Carregar um valor de registro de Language-Neutral

No Windows Vista e versões posteriores, o aplicativo MUI usa um valor de registro neutro de idioma para permitir o acesso a cadeias de caracteres específicas de idioma armazenadas em uma tabela de recursos de cadeia. Para obter mais informações, consulte criar um recurso de Language-Neutral em [usando o redirecionamento de cadeia de caracteres do registro](using-registry-string-redirection.md).

O código do aplicativo que lê o valor de idioma neutro do registro deve carregar as cadeias de caracteres no idioma correto da interface do usuário chamando [**RegLoadMUIStringW**](/windows/win32/api/winreg/nf-winreg-regloadmuistringa). Se você estiver usando essa função, seu aplicativo não precisará lidar explicitamente com o carregamento de recursos.

Se você estiver atualizando um aplicativo existente para o uso neutro de idioma do registro, normalmente manterá os valores de cadeia de caracteres existentes, localizados em inglês ou em outro idioma único no registro, como fallbacks e para compatibilidade com versões anteriores. Manter uma cadeia de caracteres literal no registro permite que o aplicativo volte para a cadeia de caracteres literal se uma chamada para [**RegLoadMUIStringW**](/windows/win32/api/winreg/nf-winreg-regloadmuistringa) falhar. Você deve decidir como implementar esse tipo de fallback, pois o MUI não oferece suporte para tal implementação.

## <a name="use-shell-api-to-set-shortcut-strings-from-the-registry"></a>Usar a API do Shell para definir as cadeias de caracteres de atalho do registro

Seu aplicativo pode usar a API do Shell para criar cadeias de caracteres para atalhos que vinculam arquivos ou pastas no menu **Iniciar** ou na área de trabalho. Para obter mais informações, consulte criar recursos para cadeias de caracteres de atalho em [usando o redirecionamento de cadeia de caracteres do registro](using-registry-string-redirection.md).

O aplicativo pode usar [**SHSetLocalizedName**](/windows/win32/api/shellapi/nf-shellapi-shsetlocalizedname) para carregar o nome de exibição compatível com MUI para um atalho. Ele deve usar [**IShellLink:: SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) para definir o InfoTip associado. As chamadas registram as cadeias de caracteres com o registro. Considere os exemplos a seguir, para os quais "HKCR" representa \_ a \_ chave do registro raiz de classes hKey:


```C++
HKCR,"CLSID\%CLSID_AntiSpyware%",,,"Windows AntiSpyware"

HKCR,"CLSID\%CLSID_AntiSpyware%","LocalizedString",,"@%ProgramFiles%\Windows AntiSpyware\MSASCui.exe,-104"

HKCR,"CLSID\%CLSID_AntiSpyware%","InfoTip",,"@%ProgramFiles%\Windows AntiSpyware\MSASCui.exe,-208"
```



A primeira linha fornece uma cadeia de caracteres literal não local para compatibilidade de fallback e de versões anteriores. A segunda linha mostra a maneira em conformidade com o MUI para registrar o nome de exibição. Essa linha indica o identificador de cadeia de caracteres 104 armazenado em Msascui.exe (para o Windows XP) ou em seu arquivo específico de idioma associado (para o Windows Vista). Esse identificador de cadeia de caracteres corresponde a "meus locais de rede". A terceira linha no exemplo manipula o registro de InfoTip. % CLSID \_ AntiSpyware% especifica uma variável de ambiente que representa o GUID que corresponde ao identificador de classe deste componente.

Para o exemplo mostrado acima, o aplicativo chama [**SHSetLocalizedName**](/windows/win32/api/shellapi/nf-shellapi-shsetlocalizedname) para especificar o caminho do executável para os dois primeiros parâmetros e especifica *idsRes* como "@% ProgramFiles% \\ Windows AntiSpyware \\MSASCui.exe, 104". Uma chamada para [**IShellLink:: SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription), especifica o caminho para o InfoTip como "@% ProgramFiles% \\ Windows antispyware \\MSASCui.exe, 208".

## <a name="query-friendly-document-type-names-in-the-registry"></a>Consultar nomes de tipo de documento amigável no registro

A criação de recursos para nomes de tipo de documento amigáveis é discutida em criar recursos para nomes de tipo de documento amigáveis [usando o redirecionamento de cadeia de caracteres do registro](using-registry-string-redirection.md) Para consultar um nome de documento amigável, o aplicativo deve usar [**IQueryAssociations:: init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init), seguido por uma chamada para [**IQueryAssociations:: GetString**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-getstring). A chamada para **IQueryAssociations:: init** especifica o tipo de documento, por exemplo, ". txt". A chamada para **IQueryAssociations:: GetString** deve especificar ASSOCSTR \_ FRIENDLYDOCNAME como o identificador de cadeia de caracteres.

## <a name="register-microsoft-management-console-snap-in-strings-not-read-from-the-registry"></a>Registrar cadeias de caracteres do snap-in do console de gerenciamento Microsoft não lidas no registro

Seu aplicativo pode usar um snap-in do MMC (console de gerenciamento Microsoft) para hospedar suas tarefas de gerenciamento. A maioria das cadeias de caracteres são tratadas como recursos usando as configurações do Registro descritas em criar recursos de cadeia de caracteres para o console de gerenciamento Microsoft Snap-Ins no [uso do redirecionamento de cadeia](using-registry-string-redirection.md) No entanto, alguns snap-ins registram valores de cadeia de caracteres do registro que o MMC não pode ler do registro. Nesse caso, o snap-in deve obter os valores usando a interface [**ISnapinAbout**](/windows/win32/api/mmc/nn-mmc-isnapinabout) , que é compatível com o MUI.

## <a name="set-the-display-name-and-description-for-a-windows-service-from-the-registry"></a>Definir o nome de exibição e a descrição de um serviço do Windows a partir do registro

Se seu aplicativo MUI estiver usando um serviço do Windows, ele deverá exibir o nome de exibição do serviço e a descrição. Os recursos associados são discutidos em "criar recursos de cadeia de caracteres para um serviço do Windows" no [usando o redirecionamento de cadeia de caracteres do registro](using-registry-string-redirection.md).

Para definir o nome de exibição do serviço, o aplicativo MUI chama [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) ou [**ChangeServiceConfig**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga). O nome é uma cadeia de caracteres no formato " `@<PE-path>,-<stringID>[;<comment>]` ". Por exemplo, se o serviço for implementado por um arquivo. dll com o caminho% ProgramFiles% \\ % MYPATH% \\MyDll.dll e o identificador da cadeia de caracteres do nome de exibição específico do idioma for 347, o parâmetro será especificado como " `@%ProgramFiles%\\%MyPath%\\MyDll.dll,-347` ". As barras invertidas duplas ( \\ \\ ) são necessárias porque o C/C++ usa a barra invertida como um caractere de escape em cadeias de caracteres.

Para definir a descrição de serviço específica do idioma, o aplicativo MUI deve fazer com que o membro **lpDescription** de uma estrutura de [**\_ Descrição de serviço**](/windows/win32/api/winsvc/ns-winsvc-service_descriptiona) indique uma cadeia de caracteres de formulário " `@<PE-path>,-<stringID>[;<comment>]` ", referenciando o identificador de cadeia de caracteres apropriado. Em seguida, o aplicativo chama [**ChangeServiceConfig2**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfig2a) com o parâmetro *dwInfoLevel* especificado como \_ Descrição da configuração do serviço \_ e o parâmetro *lpInfo* especificado como a estrutura de **\_ Descrição do serviço** .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Localizando recursos do Win32 PE](locating-win32-pe-resources.md)
</dt> <dt>

[Usando o redirecionamento de cadeia de caracteres do registro](using-registry-string-redirection.md)
</dt> </dl>

 

 
