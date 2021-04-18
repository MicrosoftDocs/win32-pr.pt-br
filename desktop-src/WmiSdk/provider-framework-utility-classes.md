---
description: As classes WMI C++ que fazem parte da estrutura do provedor WMI não são mais recomendadas para uso.
ms.assetid: d2414a72-3435-4035-bcd9-b3ec87f5709c
ms.tgt_platform: multiple
title: Classes de utilitário de estrutura de provedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab09c99fe2597cacd81e55a4ed18bd4e286ff16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771570"
---
# <a name="provider-framework-utility-classes"></a>Classes de utilitário de estrutura de provedor

\[As classes WMI C++ que fazem parte da estrutura do provedor de WMI que agora é considerada no estado final e nenhum outro desenvolvimento, melhoria ou atualização estarão disponíveis para problemas não relacionados à segurança que afetem essas bibliotecas. As [APIs de mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devem ser usadas para todo o novo desenvolvimento.\]

As bibliotecas de estrutura de provedor Framedyd.dll (versão de depuração) e Framedyn.dll (versão de lançamento) implementam várias classes auxiliares de provedor. Algumas funções no Framedyn.dll foram removidas dos arquivos de cabeçalho. Para continuar a usar essas funções, adicione `#define FRAMEWORK_ALLOW_DEPRECATED` ao seu código antes de incluir Fwcommon. h.

Você pode descarregar provedores individuais que não são mais necessários.

Para usar essa funcionalidade, você deve fazer as três alterações a seguir em seu provedor em MainDll. cpp:

-   Na função **DllMain** em que você chama [**CWbemProviderGlue:: FrameworkLoginDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogindll(lpcwstr_plong)), você deve adicionar um segundo parâmetro que é um ponteiro para um longo.
-   Na função **DllCanUnloadNow** em que você chama [**CWbemProviderGlue:: FrameworkLogoffDLL**](/windows/desktop/api/WbemGlue/nf-wbemglue-cwbemproviderglue-frameworklogoffdll(lpcwstr_plong)), você deve adicionar um segundo parâmetro que é um ponteiro para um longo.
-   Na função **DllGetClassObject** em que você cria uma instância de **CWbemGlueFactory**, você deve adicionar um parâmetro que é um ponteiro para um longo.

Em todos os três casos, o ponteiro para um longo deve ser o mesmo ponteiro.

> [!Note]  
> Nas rotinas Maindll. cpp, **DllGetClassObject**, **DllCanUnloadNow**, **DllRegisterServer**, **DllUnregisterServer** e **DllMain** devem ser encapsuladas em um bloco try/catch.

 

> [!Caution]  
> A depuração do provedor cria o link com Framedyd. lib para Framedyd.dll. Framedyd.dll está no diretório bin do SDK (Software Development Kit) do Microsoft Windows \\ que não está incluído no caminho do sistema. Quando uma compilação de depuração de um provedor é testada com o serviço de gerenciamento do Windows, o provedor de estrutura não será carregado porque Framedyd.dll ou uma de suas dependências não será localizada. Portanto, você deve copiar Framedyd.dll do \\ diretório SDK do Windows bin para o diretório system32 do \\ \\ ou adicionar o \\ diretório bin do SDK do Windows ao caminho de pesquisa do sistema.

 

A tabela a seguir lista as classes de utilitário de estrutura de provedor.



| Classe de utilitário                                          | Descrição                                                                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**CHString**](chstring.md)                           | Fornece comparação de cadeias de caracteres e funções de manipulação para o WMI.                                                                  |
| [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray)                 | Contém para criar e manipular matrizes de CHString.                                                                      |
| [**TRefPointerCollection**](/windows/desktop/api/RefPtrCo/nl-refptrco-trefpointercollection) | Concede acesso a uma classe de contêiner para ponteiros.                                                                                |
| [**WBEMTime**](wbemtime.md)                           | Facilita conversões entre vários formatos de tempo de execução do Windows e ANSI C.                                               |
| [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan)                   | Contém funções auxiliares usadas para calcular e manter a diferença de intervalo de tempo entre dois objetos [**WBEMTime**](wbemtime.md) . |



 

> [!Note]  
> As classes [**CHString**](chstring.md) e [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) são semelhantes às MFC (MFC) **CString** e **CStringArray**. As versões do WMI existem para que os desenvolvedores possam acessar os métodos de comparação e de manipulação de cadeia de caracteres sem precisar acessar o MFC. As classes [**WBEMTime**](wbemtime.md) e [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) também são semelhantes às classes MFC **CTime** e **CTimeSpan** . As versões do WMI são capazes de armazenar a precisão do tempo em nanossegundos e também podem converter de e para o **BSTR**. Para obter mais informações sobre as classes CString, CStringArray, CTime e CTimeSpan, consulte o [MFC](https://msdn.microsoft.com/library/d06h2x6e(VS.71).aspx) no msdn.

 

Valores **BSTR** retornados por métodos [**WBEMTime**](wbemtime.md) estão no [formato de data e hora](date-and-time-format.md): "AAAAMMDDHHMMSS. mmmmmmsUUU"

Valores **BSTR** retornados por métodos [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan) estão no [formato de intervalo](interval-format.md): "ddddddddHHMMSS. mmmmmm: 000"

Embora os tempos e os intervalos de tempo sejam armazenados internamente como nanossegundos, eles não são necessariamente armazenados com precisão de nanossegundos. Isso ocorre porque os objetos [**WBEMTime**](wbemtime.md) podem ser construídos usando formatos de tempo que são precisos para um segundo (**struct tm** e **time \_ t**). Adicionar casas decimais artificiais não aumenta a precisão.

 

 
