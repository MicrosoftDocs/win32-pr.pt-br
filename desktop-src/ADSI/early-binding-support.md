---
title: Suporte de associação antecipada
description: O exemplo de código a seguir apresenta um cenário com suporte de associação antecipada em vigor.
ms.assetid: 3ca955cc-a9cd-4309-8617-89fe50b65c3d
ms.tgt_platform: multiple
keywords:
- ADSI de extensões, suporte de ligação antecipada
- Associação de anúncio, suporte de associação antecipada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be6980edb0395ad0139f9cf2e4a1f9cde3ff6077
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084893"
---
# <a name="early-binding-support"></a>Suporte de associação antecipada

O exemplo de código a seguir apresenta um cenário com suporte de associação antecipada em vigor.


```VB
Dim x as IADsUser
Dim y as IADsExt1
Dim z as IADsExt2
 
Set x = GetObject("LDAP://CN=JeffSmith, OU=Sales, 
                   DC=Fabrikam,DC=COM")
x.SetPassword("newPassword")
 
Set y = x
y.MyNewMethod( "\\srv\public")
y.MyProperty = "Hello World"
 
Set z = y
z.OtherMethod()
z.OtherProperty = 4362
 
Debug.Print x.LastName
 
Set z = GetObject("LDAP://CN=Jeff,OU=Engr, 
                   DC=Fabrikam,DC=COM")
z.OtherProperty = 5323
```



Neste exemplo de código, dois componentes de extensão estendem um objeto de **usuário** . Cada extensão publica sua própria interface. Cada extensão não reconhece a outra interface de extensão; somente ADSI reconhece a existência de ambas as extensões. Cada extensão Delega seu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) a ADSI. A ADSI atua como um agregador para ambas as extensões e outras extensões futuras. Consultar uma interface de qualquer extensão ou de ADSI, produz o mesmo resultado consistente.

O procedimento a seguir descreve como criar uma extensão.

## <a name="step-1-add-aggregation-to-your-component"></a>Etapa 1: Adicionar agregação ao seu componente

Siga a especificação COM para adicionar agregação ao seu componente. Em resumo, você deve aceitar as solicitações *pUnknown* para o componente durante **CreateInstance** e delegar o *pUnknown* ao [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do agregador se o componente for agregado.

## <a name="step-2-register-your-extension"></a>Etapa 2: registrar sua extensão

Agora você deve decidir qual classe de diretório estender. Não é possível usar as mesmas interfaces para fazer isso que você usaria para uma interface ADSI, por exemplo, [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer). Os objetos de diretório são mantidos no diretório, enquanto a extensão e a ADSI estão em execução no computador cliente. Os exemplos de objeto de diretório são **User**, **Computer**, **PrintQueue**, **serviceConnectionPoint** e **nTDSService**. Você pode adicionar uma nova classe em Active Directory e criar uma nova extensão para essa nova classe também.

Você usa chaves do registro para associar um nome de classe de diretório com os componentes de extensão ADSI. A figura a seguir representa o layout de registro existente, bem como novas chaves.

-   Uma nova chave, chamada **extensões**, contém uma lista de chaves, cada uma representando uma classe no diretório. Cada classe, por exemplo, **User**, **PrintQueue** ou **Computer**, mantém uma lista de subchaves.
-   Cada subchave contém o CLSID do componente de extensão ADSI.
-   Cada subchave CLSID contém uma entrada de cadeia de caracteres que permite vários valores. Você só deve listar as interfaces que participam da agregação.

> [!Note]  
> Os objetos de extensão ainda são necessários para registrar chaves COM padrão.

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         ADS
            Providers
               LDAP
                  Extensions
                     ClassNameA
                        CLSID of ExtensionA1
                           Interfaces = List of interfaces
                        CLSID of ExtensionA2
                           Interfaces = List of interfaces
                     ClassNameB
                        CLSID of ExtensionB1
                           Interfaces = List of interfaces
                        CLSID of ExtensionB2
                           Interfaces = List of interfaces
```

## <a name="example"></a>Exemplo

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               LDAP
                  Extensions
                     printQueue
                        {9f37f39c-6f49-11d1-8c18-00c04fd8d503}
                           Interfaces = {466841B0-E531-11d1-8718-00C04FD44407}
                                        {466841B1-E531-11d1-8718-00C04FD44407}
```

A lista de interfaces do Extension1 pode ser diferente da do Extension2. O objeto, quando ativo, dá suporte às interfaces do agregador (ADSI) e a todas as interfaces fornecidas pelo Extension1 e Extension2 da agregação. A resolução de interfaces conflitantes (a mesma interface com suporte tanto pelo agregador quanto pelas agregações ou por várias agregações) é determinada pelas prioridades das extensões.

Você também pode associar sua extensão CLSID a vários nomes de classe de objeto. Por exemplo, sua extensão pode estender os objetos de **usuário** e de **contato** .

> [!Note]  
> O comportamento da extensão é adicionado em uma classe por objeto, não em uma instância por objeto.

 

Como prática recomendada, registre suas extensões, como você faria com qualquer outro componente COM, com uma chamada para a função **DllRegisterSvr** . Além disso, forneça um recurso para cancelar o registro de sua extensão com a função **DllUnregisterServer** .

O exemplo de código a seguir mostra como registrar uma extensão.


```C++
/////
// Register the class.
///////////////////////
hr = RegCreateKeyEx( HKEY_LOCAL_MACHINE,
                 _T("SOFTWARE\\Microsoft\\ADs\\Providers\\LDAP\\Extensions\\User\\{E1E3EDF8-48D1-11D2-B22B-0000F87A6B50}"),
 0,
 NULL,
 REG_OPTION_NON_VOLATILE,
 KEY_WRITE,
 NULL,
 &hKey,
 &dwDisposition );
 
///////////////////////////
// Register the Interface.
///////////////////////////
const TCHAR szIf[] = _T("{E1E3EDF7-48D1-11D2-B22B-0000F87A6B50}");
 
hr = RegSetValueEx( hKey, _T("Interfaces"), 0, REG_BINARY, (const BYTE *) szIf, sizeof(szIf) );
 
RegCloseKey(hKey);
return S_OK;
 
}
```



 

 