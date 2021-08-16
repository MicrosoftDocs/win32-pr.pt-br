---
description: Este tópico discute instruções de programação para localizar cadeias de caracteres do Registro redirecionadas. Para obter mais informações, consulte Usando o redirecionamento de cadeia de caracteres do Registro.
ms.assetid: 03d1512f-35a6-4b3a-9a0e-97e17bd9b126
title: Localizando cadeias de caracteres redirecionadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9c4e1a46b2c12af839e4c5b562eba18a80c8e814e5a6071dca925a14a46d0ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788476"
---
# <a name="locating-redirected-strings"></a>Localizando cadeias de caracteres redirecionadas

Este tópico discute instruções de programação para localizar cadeias de caracteres do Registro redirecionadas. Para obter mais informações, consulte [Usando o redirecionamento de cadeia de caracteres do Registro](using-registry-string-redirection.md).

## <a name="load-a-language-neutral-registry-value"></a>Carregar um Language-Neutral do Registro

No Windows Vista e posterior, o aplicativo MUI usa um valor de registro neutro em idioma para permitir o acesso a cadeias de caracteres específicas de idioma armazenadas em uma tabela de recursos de cadeia de caracteres. Para obter mais informações, consulte Create a Language-Neutral resource in [Using Registry String Redirection](using-registry-string-redirection.md).

O código do aplicativo que lê o valor neutro de idioma do Registro deve carregar as cadeias de caracteres na linguagem de interface do usuário correta chamando [**RegLoadMUIStringW**](/windows/win32/api/winreg/nf-winreg-regloadmuistringa). Se estiver usando essa função, seu aplicativo não precisa lidar explicitamente com o carregamento de recursos.

Se você estiver atualizando um aplicativo existente para o uso neutro do idioma do Registro, normalmente manterá os valores de cadeia de caracteres existentes, localizados em inglês ou em algum outro idioma único no Registro, como fallbacks e para compatibilidade com backward. Manter uma cadeia de caracteres literal no Registro permite que o aplicativo volte para a cadeia de caracteres literal se uma chamada para [**RegLoadMUIStringW**](/windows/win32/api/winreg/nf-winreg-regloadmuistringa) falhar. Você deve decidir como implementar esse fallback, pois a MUI não oferece suporte para tal implementação.

## <a name="use-shell-api-to-set-shortcut-strings-from-the-registry"></a>Usar a API do Shell para definir cadeias de caracteres de atalho do Registro

Seu aplicativo pode usar a API do shell para criar cadeias de caracteres para atalhos que vinculam arquivos ou pastas no **menu** Iniciar ou na área de trabalho. Para obter mais informações, consulte Criar recursos para cadeias de caracteres de atalho em [Usando o redirecionamento de cadeia de caracteres do Registro](using-registry-string-redirection.md).

O aplicativo pode usar [**SHSetLocalizedName**](/windows/win32/api/shellapi/nf-shellapi-shsetlocalizedname) para carregar o nome de exibição em conformidade com a MUI para um atalho. Ele deve usar [**IShellLink::SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) para definir o InfoTip associado. As chamadas registram as cadeias de caracteres com o Registro. Considere os exemplos a seguir, para os quais "HKCR" representa a chave do Registro RAIZ de \_ CLASSES HKEY: \_


```C++
HKCR,"CLSID\%CLSID_AntiSpyware%",,,"Windows AntiSpyware"

HKCR,"CLSID\%CLSID_AntiSpyware%","LocalizedString",,"@%ProgramFiles%\Windows AntiSpyware\MSASCui.exe,-104"

HKCR,"CLSID\%CLSID_AntiSpyware%","InfoTip",,"@%ProgramFiles%\Windows AntiSpyware\MSASCui.exe,-208"
```



A primeira linha fornece uma cadeia de caracteres literal não alocada para compatibilidade com fallback e compatibilidade com compatibilidade. A segunda linha mostra a maneira compatível com a MUI de registrar o nome de exibição. Essa linha indica o identificador de cadeia de caracteres 104 armazenado no Msascui.exe (para Windows XP) ou em seu arquivo específico de idioma associado (para Windows Vista). Esse identificador de cadeia de caracteres corresponde a "Meus Locais de Rede". A terceira linha no exemplo lida com o registro de InfoTip. %CLSID AntiSpyware% especifica uma variável de ambiente que representa o GUID que corresponde ao \_ identificador de classe desse componente.

Para o exemplo mostrado acima, o aplicativo chama [**SHSetLocalizedName**](/windows/win32/api/shellapi/nf-shellapi-shsetlocalizedname) para especificar o caminho do executável para os dois primeiros parâmetros e especificar *idsRes* como "@%ProgramFiles% \\ Windows AntiSpyware \\MSASCui.exe,104". Uma chamada para [**IShellLink::SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription)especifica o caminho para o InfoTip como "@%ProgramFiles% \\ Windows AntiSpyware \\MSASCui.exe,208".

## <a name="query-friendly-document-type-names-in-the-registry"></a>Consultar nomes de tipo de documento amigáveis no Registro

A criação de recursos para nomes de tipo de documento amigáveis é discutida em Criar recursos para nomes de tipo de documento amigáveis em Usando o redirecionamento de cadeia [de caracteres do Registro](using-registry-string-redirection.md). Para consultar um nome de documento amigável, o aplicativo deve usar [**IQueryAssociations::Init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init), seguido por uma chamada para [**IQueryAssociations::GetString**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-getstring). A chamada para **IQueryAssociations::Init** especifica o tipo de documento, por exemplo, ".txt". A chamada para **IQueryAssociations::GetString** deve especificar ASSOCSTR \_ FRIENDLYDOCNAME como o identificador de cadeia de caracteres.

## <a name="register-microsoft-management-console-snap-in-strings-not-read-from-the-registry"></a>Registrar Console de Gerenciamento Microsoft cadeias de caracteres snap-in não lidas do Registro

Seu aplicativo pode usar um snap-in Console de Gerenciamento Microsoft (MMC) para hospedar suas tarefas de gerenciamento. A maioria das cadeias de caracteres é tratada como recursos usando as configurações do Registro descritas em Criar recursos de cadeia de caracteres para Console de Gerenciamento Microsoft Snap-Ins usando redirecionamento de cadeia de [caracteres do Registro](using-registry-string-redirection.md). No entanto, alguns snap-ins registram valores de cadeia de caracteres do Registro que o MMC não pode ler do Registro. Nesse caso, o snap-in deve obter os valores usando a interface [**ISnapinAbout,**](/windows/win32/api/mmc/nn-mmc-isnapinabout) que é compatível com MUI.

## <a name="set-the-display-name-and-description-for-a-windows-service-from-the-registry"></a>Definir o nome de exibição e a descrição de um Windows do Registro

Se o aplicativo MUI estiver usando um serviço Windows, ele deverá exibir o nome de exibição e a descrição do serviço. Os recursos associados são discutidos em "Criar recursos de cadeia de caracteres para um serviço Windows" em Usando o redirecionamento de cadeia [de caracteres do Registro](using-registry-string-redirection.md).

Para definir o nome de exibição do serviço, o aplicativo MUI [**chama CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) ou [**ChangeServiceConfig**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga). O nome é uma cadeia de caracteres do formato " `@<PE-path>,-<stringID>[;<comment>]` ". Por exemplo, se o serviço for implementado por um arquivo .dll com o caminho %ProgramFiles% %MyPath%MyDll.dll e o identificador de cadeia de caracteres do nome de exibição específico do idioma for \\ 347, o parâmetro será especificado \\ como " `@%ProgramFiles%\\%MyPath%\\MyDll.dll,-347` ". As malhas invertida duplas ( ) são necessárias porque o C/C++ usa a faixa invertida como um caractere de \\ \\ escape em cadeias de caracteres.

Para definir a descrição de serviço específica do idioma, o aplicativo MUI deve fazer com que o membro **lpDescription** de uma estrutura [**SERVICE \_ DESCRIPTION**](/windows/win32/api/winsvc/ns-winsvc-service_descriptiona) indique uma cadeia de caracteres do formato " ", referenciando o identificador de cadeia de caracteres `@<PE-path>,-<stringID>[;<comment>]` apropriado. Em seguida, o aplicativo chama [**ChangeServiceConfig2**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfig2a) com o parâmetro *dwInfoLevel* especificado como SERVICE CONFIG DESCRIPTION e o parâmetro lpInfo especificado como \_ a estrutura SERVICE \_ **\_ DESCRIPTION.** 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Localizando recursos do Win32 PE](locating-win32-pe-resources.md)
</dt> <dt>

[Usando o redirecionamento de cadeia de caracteres do Registro](using-registry-string-redirection.md)
</dt> </dl>

 

 
