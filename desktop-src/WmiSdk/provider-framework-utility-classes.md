---
description: As classes WMI C++ que fazem parte do WMI Provider Framework não são mais recomendadas para uso.
ms.assetid: d2414a72-3435-4035-bcd9-b3ec87f5709c
ms.tgt_platform: multiple
title: Classes de utilitário do Provider Framework
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 254a1321ab835c86e7b4bf0e5cb14048be0352290707a61aaf993a9a6cc6e8dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130978"
---
# <a name="provider-framework-utility-classes"></a>Classes de utilitário do Provider Framework

\[As classes WMI C++ que fazem parte do WMI Provider Framework, que agora é considerada no estado final, e nenhum desenvolvimento, aprimoramentos ou atualizações adicionais estarão disponíveis para problemas não relacionados à segurança que afetam essas bibliotecas. As [APIs de MI](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]

As bibliotecas de estrutura do provedor Framedyd.dll (versão de depuração) e Framedyn.dll (versão de versão) implementam várias classes auxiliares do provedor. Algumas funções no Framedyn.dll foram removidas dos arquivos de header. Para continuar a usar essas funções, adicione `#define FRAMEWORK_ALLOW_DEPRECATED` ao código antes de incluir Fwcommon.h.

Você pode descarregar provedores individuais que não são mais necessários.

Para usar essa funcionalidade, você deve fazer as três alterações a seguir em seu provedor em MainDll.cpp:

-   Na função **DllMain** em que você chama [**CWbemProviderGlue::FrameworkLoginDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogindll(lpcwstr_plong)), você deve adicionar um segundo parâmetro que é um ponteiro para um long.
-   Na função **DllCanUnloadNow** em que você chama [**CWbemProviderGlue::FrameworkLogoffDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogoffdll(lpcwstr_plong)), você deve adicionar um segundo parâmetro que é um ponteiro para um long.
-   Na função **DllGetClassObject** em que você cria uma instância **de CWbemGlueFactory**, você deve adicionar um parâmetro que é um ponteiro para um long.

Em todos os três casos, o ponteiro para um long deve ser o mesmo ponteiro.

> [!Note]  
> No Maindll.cpp, as rotinas **DllGetClassObject**, **DllCanUnloadNow**, **DllRegisterServer**, **DllUnregisterServer** e **DllMain** devem ser envolvidas em um bloco try/catch.

 

> [!Caution]  
> Link de builds de depuração do provedor com Framedyd.lib para Framedyd.dll. Framedyd.dll está no diretório bin do Microsoft Windows Software Development Kit (SDK), que não \\ está incluído no caminho do sistema. Quando um build de depuração de um provedor for testado com o serviço Windows Management, o provedor de estrutura não será carregado porque Framedyd.dll ou uma de suas dependências não estará localizada. Portanto, você deve copiar Framedyd.dll do diretório bin do SDK do Windows para o diretório \\ wbem do system32 ou adicionar o diretório bin do SDK do Windows ao caminho de pesquisa do \\ \\ \\ sistema.

 

A tabela a seguir lista as classes de utilitário da estrutura do provedor.



| Classe de utilitário                                          | Descrição                                                                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**CHString**](chstring.md)                           | Fornece funções de comparação e manipulação de cadeia de caracteres para WMI.                                                                  |
| [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray)                 | Contém para criar e manipular matrizes de CHString.                                                                      |
| [**TRefPointerCollection**](/windows/desktop/api/RefPtrCo/nl-refptrco-trefpointercollection) | Concede acesso a uma classe de contêiner para ponteiros.                                                                                |
| [**WBEMTime**](wbemtime.md)                           | Facilita conversões entre vários Windows formatos de tempo de run time do ANSI C.                                               |
| [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan)                   | Contém funções auxiliares usadas para calcular e manter a diferença de intervalo de tempo entre dois [**objetos WBEMTime.**](wbemtime.md) |



 

> [!Note]  
> As [**classes CHString**](chstring.md) e [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) são semelhantes às MFC (MFC) **CString** e **CStringArray**. As versões do WMI existem para que os desenvolvedores possam acessar métodos de comparação e manipulação de cadeia de caracteres sem precisar acessar o MFC. As [**classes WBEMTime**](wbemtime.md) e [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) também são semelhantes às classes **CTime** e **CTimeSpan** do MFC. As versões WMI são capazes de armazenar tempo para precisão de nanossegundos e também podem converter para e de **BSTR**. Para obter mais informações sobre as classes CString, CStringArray, CTime e CTimeSpan, consulte o [MFC](https://msdn.microsoft.com/library/d06h2x6e(VS.71).aspx) no MSDN.

 

**Os valores BSTR** retornados pelos métodos [**WBEMTime**](wbemtime.md) estão no formato [de](date-and-time-format.md)data e hora: "aaaammddHHMMSS.mmmmmmsUUU"

**Os valores BSTR** retornados pelos métodos [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) estão no formato [interval](interval-format.md): "dddddddddHHMMSS.mmmmmm:000"

Embora os tempos e intervalos de tempo sejam armazenados internamente como nanossegundos, eles não são necessariamente armazenados com precisão de nanossegundos. Isso porque os [**objetos WBEMTime**](wbemtime.md) podem ser construídos usando formatos de tempo precisos para um segundo (**struct tm** e **time \_ t**). Adicionar casas decimais artificiais não aumenta a precisão.

 

 
