---
description: assim como outros provedores de instância, você registra um provedor de alto desempenho com o Microsoft Windows&\# 160; Instrumentação de gerenciamento (WMI) criando uma instância das \_ \_ classes Win32Provider e \_ \_ InstanceProviderRegistration.
ms.assetid: 6ff3f8c6-71ca-4589-bca7-b864e24a473d
ms.tgt_platform: multiple
title: Registrando um provedor de High-Performance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ee52db95290810a046d23781dbccf666cd63a19b01bf9414b2e224b8137f8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992566"
---
# <a name="registering-a-high-performance-provider"></a>Registrando um provedor de High-Performance

assim como outros provedores de instância, você registra um provedor de alto desempenho com o Microsoft Instrumentação de Gerenciamento do Windows (WMI) criando uma instância das classes [**\_ \_ win32provider**](--win32provider.md) e [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) . A instância do **\_ \_ Win32Provider** define a implementação física do provedor e a instância **\_ \_ InstanceProviderRegistration** define o conjunto de recursos do provedor. Para obter mais informações, consulte [registrando um provedor](registering-a-provider.md).

O procedimento a seguir descreve como registrar um provedor de instância de alto desempenho.

**Para registrar um provedor de instância de alto desempenho**

1.  Crie uma instância da classe [**\_ \_ Win32Provider**](--win32provider.md) que descreve o provedor.

    Certifique-se de adicionar uma propriedade **ClientLoadableCLSID** à instância [**\_ \_ Win32Provider**](--win32provider.md) . Se o provedor e o cliente residirem no mesmo computador, o WMI carregará o provedor em processo para o cliente usando **ClientLoadableCLSID** como o identificador de classe. Quando o provedor e o cliente residem em computadores diferentes, o WMI carrega o provedor em processo para o WMI. O WMI também usa **ClientLoadableCLSID** para dar suporte a operações de atualização.

2.  Crie uma instância da classe [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) que descreve o conjunto de recursos do provedor.

    Certifique-se de marcar a classe com os qualificadores [**dinâmicos**](dynamic-qualifier.md) e de [**provedor**](/windows/desktop/api/Provider/nl-provider-provider) . O qualificador **dinâmico** sinaliza que o WMI deve usar um provedor para recuperar as instâncias de classe. O qualificador do **provedor** especifica o nome do provedor que o WMI deve usar.

    Um provedor de alto desempenho também precisa de um estado de suporte para operações, operações de enumeração ou ambos. Certifique-se de usar as propriedades **SupportsGet** e **SupportsEnumeration** em sua implementação.

O exemplo de código a seguir mostra como implementar as classes [**\_ \_ Win32Provider**](--win32provider.md) e [**\_ \_ InstanceProviderRegistration**](--instanceproviderregistration.md) para um provedor de alto desempenho.

``` syntax
instance of __Win32Provider as $P
{
    Name="TestProv";
    CLSID="{A41602A4-C038-11d1-AEB6-00C04FB68820}";
    ClientLoadableCLSID="{423B32C9-B033-4242-EFB6-55C044242821}";
};

instance of __InstanceProviderRegistration
{
    Provider = $P;
    SupportsGet = TRUE;
    SupportsEnumeration = TRUE;
};

[ dynamic, 
  provider("TestProv")
]

class TestClass
{
    [key] string KeyVal;
    
    string StrVal1;

    sint32 IntVal1;
    sint32 IntVal2;

    sint32 IntArray2[];
};
```

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando um provedor de instância em um provedor de High-Performance](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



