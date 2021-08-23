---
description: O serviço de autenticação Kerberos especifica o nome principal do servidor para garantir a identidade do computador ao qual ele está se conectando.
ms.assetid: 3d58db28-2e69-4e27-9f27-61529abbf750
ms.tgt_platform: multiple
title: Especificando o nome principal do servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc8b3d05d6933653a7d2a1737d36f00f6ca65c39bd7739e5f2e9f4232eb507f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816419"
---
# <a name="specifying-the-server-principal-name"></a>Especificando o nome principal do servidor

O serviço de autenticação Kerberos especifica o nome principal do servidor para garantir a identidade do computador ao qual ele está se conectando. Especifique o nome principal do servidor na chamada para o método de script [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) fornecendo o nome do computador remoto. Em C++, especifique o nome principal do servidor no parâmetro *pServerPrincName* ao chamar [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) para o proxy. Para obter mais informações, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).

Esse parâmetro é necessário para que o Kerberos dê suporte à autenticação mútua. No entanto, o uso do nome principal do servidor padrão não permite a autenticação mútua. Os clientes para os quais a autenticação mútua é crítica devem especificar um nome principal de servidor que corresponda à identidade do servidor que o serviço WMI está usando. Para obter mais informações sobre como configurar a segurança de proxy e um exemplo de C++ mostrando como definir o nome principal do servidor, consulte [definindo a segurança em IWbemServices e em outros proxies](setting-the-security-on-iwbemservices-and-other-proxies.md).

para obter mais informações sobre como definir o nome principal do servidor em script e Visual Basic, consulte [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) e [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).

ao contrário da maioria dos protocolos de segurança para Instrumentação de Gerenciamento do Windows (WMI) e Component Object Model (COM), você não pode definir a entidade do servidor em uma chamada para [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity). No entanto, você pode definir a entidade de segurança do servidor com o parâmetro *bstrAuthority* para [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver)ou o parâmetro *pServerPrincName* para [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).

O exemplo de código neste tópico requer a seguinte \# instrução include para compilação correta.


```C++
#include <wbemidl.h>
```



O exemplo de código a seguir mostra como definir o nome principal do servidor com [**ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver).


```C++
IWbemServices* g_pNameSpace = NULL;

// Namespace to which to connect
BSTR  bstrNameSpace = 
SysAllocString( L"\\\\MyMachine\\root\default" );

// The bstrAuthority string contains the server
// principal name MyDomain\\MyMachine
// and the authentication service, which is Kerberos.
BSTR  bstrAuthority = 
SysAllocString( L"kerberos:MyDomain\\MyMachine"  );

HRESULT hr = NULL;
IWbemLocator* pWbemLocator = 0;

  hr = pWbemLocator->ConnectServer(
          bstrNameSpace,  // NameSpace name
          NULL,           // User name
          NULL,           // Password
          NULL,           // Locale
          0L,             // Security flags
          bstrAuthority,  // Authority, server principal name
          NULL,           // WBEM context
          &g_pNameSpace   // Namespace
          );

  // Free memory resources.
  g_pNameSpace->Release();
  SysFreeString(bstrNameSpace);
  SysFreeString(bstrAuthority);
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando o serviço de autenticação usando o VBScript](setting-the-authentication-service-using-vbscript.md)
</dt> <dt>

[Configurando a autenticação usando C++](setting-authentication-using-c-.md)
</dt> <dt>

[Definindo a segurança em IWbemServices e em outros proxies](setting-the-security-on-iwbemservices-and-other-proxies.md)
</dt> </dl>

 

 
