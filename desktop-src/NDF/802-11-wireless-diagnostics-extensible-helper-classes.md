---
title: 802,11 classes auxiliares extensíveis de diagnóstico sem fio
description: A infraestrutura interna de diagnóstico sem fio tem dois pontos de extensão. Auxiliar ClassPurposeRevised nativo Wi-Fi (RNWF) extensível auxiliar ClassDiagnoses problemas relacionados a extensões de conectividade 802,11.
ms.assetid: b54f836d-4fae-4e71-bf7b-af5a6e9e615c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3b7ac72cb42b12a96e5c57db0897a13d49d76370126e119ac2f5ed457d55c9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133441"
---
# <a name="80211-wireless-diagnostics-extensible-helper-classes"></a>802,11 classes auxiliares extensíveis de diagnóstico sem fio

A infraestrutura interna de diagnóstico sem fio tem dois pontos de extensão.

| Classe auxiliar pai                                | Finalidade                                                           |
|----------------------------------------------------|-------------------------------------------------------------------|
| Classe auxiliar extensível RNWF (WiFi nativo) revisada | Diagnostica problemas relacionados a extensões de conectividade 802,11.       |
| Classe auxiliar extensível L2Security                 | Diagnostica problemas relacionados às extensões do protocolo de segurança de camada 2. |



 

> [!Note]  
> Uma classe auxiliar de terceiros deve se registrar com ambas as classes auxiliares pai para garantir que a classe de terceiros seja chamada. Para obter mais informações sobre o registro, consulte [registrando extensões de classe auxiliar NDF](registering-ndf-helper-class-extensions.md).

 

## <a name="rnwf-extensible-helper-class"></a>Classe auxiliar extensível RNWF

Nome da classe auxiliar pai

``` syntax
Parent = L"RNWF Extensible Helper Class";
```

A classe auxiliar extensível RNWF (WiFi nativo) revisada é o pai para classes auxiliares de terceiros que diagnosticam problemas relacionados à extensão de protocolos 802,11 usados por Wi-Fi nativo.

Os dois atributos de chave fornecidos pela classe auxiliar RNWF são o GUID da interface em que o problema ocorreu e o contexto de conexão.

-   GUID da interface: esse atributo é denominado "ID da interface" e é do tipo **em \_ GUID**.

-   Contexto de conexão: esse atributo é denominado ID de rede e é do \_ tipo \_ cadeia de caracteres de octeto. Essa cadeia de caracteres é, na verdade, um buffer da \_ estrutura de ID da WLAN WDIAG IHV \_ \_ definida em Wlanihv. h. Essa estrutura é definida da seguinte maneira.

    ``` syntax
#define WDIAG_IHV_WLAN_ID_FLAG_SECURITY_ENABLED               0x00000001
    typedef
    struct _WDIAG_IHV_WLAN_ID
    {
        WCHAR                        strProfileName [MS_MAX_PROFILE_NAME_LENGTH];
        DOT11_SSID                   Ssid;
        DOT11_BSS_TYPE               BssType;
        DWORD                        dwFlags;           // Flags defined above
        DWORD                        dwReasonCode;      // Set only when an applicable reason code is available
    }
    WDIAG_IHV_WLAN_ID, *PWDIAG_IHV_WLAN_ID;
    ```

> [!Note]  
> **WDIAG \_ A \_ segurança do sinalizador de ID da WLAN do IHV \_ \_ \_ \_ habilitada** é o único valor de **dwFlags** possível.

 

O atributo correspondente para a classe auxiliar de terceiros deve ser igual à ID de serviço do seu módulo de software correspondente. Esse também é o mesmo nome que a terceira parte deve ser registrada no registro. O diagnóstico sem fio consultará a ID do serviço durante a sessão sem fio em que o problema ocorreu. As informações serão retornadas para NDF, que determinará se a classe auxiliar de terceiros está presente e registrada e, em seguida, a chama.

A tabela a seguir lista os atributos correspondentes para a classe auxiliar extensível RNWF.



| Nome          | Tipo    | Valor                         |
|---------------|---------|-------------------------------|
| Diagnosticsid | REG \_ sz | \[Cadeia de \_ caracteres de GUID diagnosticsid \_ |



 

## <a name="l2security-extensible-helper-class"></a>Classe auxiliar extensível L2Security

Nome da classe auxiliar pai

``` syntax
Parent = L"Extensible L2Sec Helper Class";
```

A classe auxiliar extensível de segurança de camada 2 (L2Security) é o pai para classes auxiliares de terceiros que diagnosticam problemas relacionados a serviços correspondentes e módulos de software que substituem a funcionalidade de segurança de camada 2.

Os dois atributos de chave fornecidos pela classe auxiliar de segurança de camada 2 são o GUID da interface em que o problema ocorreu e o contexto de conexão.

-   GUID da interface: esse atributo é denominado "ID da interface" e é do tipo **em \_ GUID**.

-   Contexto de conexão: esse atributo é denominado ID de rede e é do \_ tipo \_ cadeia de caracteres de octeto. Essa cadeia de caracteres é, na verdade, um buffer da \_ estrutura de ID da WLAN WDIAG IHV \_ \_ definida em wlanihv. h. Essa estrutura é definida da seguinte maneira.

    ``` syntax
#define WDIAG_IHV_WLAN_ID_FLAG_SECURITY_ENABLED               0x00000001
    typedef
    struct _WDIAG_IHV_WLAN_ID
    {
        WCHAR                        strProfileName [MS_MAX_PROFILE_NAME_LENGTH];
        DOT11_SSID                   Ssid;
        DOT11_BSS_TYPE               BssType;
        DWORD                        dwFlags;           // Flags defined above
        DWORD                        dwReasonCode;      // Set only when an applicable reason code is available
    }
    WDIAG_IHV_WLAN_ID, *PWDIAG_IHV_WLAN_ID;
    ```

> [!Note]  
> **WDIAG \_ A \_ segurança do sinalizador de ID da WLAN do IHV \_ \_ \_ \_ habilitada** é o único valor de **dwFlags** possível.

 

O atributo correspondente para a classe auxiliar de terceiros deve ser igual à ID de serviço do seu módulo de software correspondente. Esse também é o mesmo nome que a terceira parte deve ser registrada no registro. O diagnóstico sem fio consultará a ID do serviço durante a sessão sem fio em que o problema ocorreu. As informações serão retornadas para NDF, que determinará se a classe auxiliar de terceiros está presente e registrada e, em seguida, a chama.

A tabela a seguir lista os atributos correspondentes para a classe auxiliar extensível de segurança de camada 2.



| Nome          | Tipo    | Valor                         |
|---------------|---------|-------------------------------|
| Diagnosticsid | REG \_ sz | \[Cadeia de \_ caracteres de GUID diagnosticsid \_ |



 

## <a name="matching-attributes"></a>Atributos correspondentes

**Diagnosticsid**

802,11 o diagnóstico sem fio consultará o *diagnosticsid* do serviço de Wi-Fi nativo básico para descobrir se alguma extensão ou módulo de segurança de terceiros está instalado e envolvido na conexão. O diagnóstico sem fio, em seguida, fornecerá as subclasses a essas classes auxiliares de terceiros usando o *diagnosticsid* como o atributo correspondente. Todas as classes auxiliares de terceiros devem ser incluídas no e instaladas com o pacote de driver associado. O *diagnosticsid* será definido no arquivo INF da miniporta como uma chave do registro na diretiva [AddReg](https://msdn.microsoft.com/library/ms794514.aspx) .

``` syntax
HKR,Ndi\IHVExtensions, DiagnosticsID,0, "<Diagnostics ID GUID>"
```

Essa chave define a ID da classe auxiliar sem fio para o módulo de software de terceiros. Essa chave é opcional para a estrutura de extensibilidade, mas é necessária se a implementação inclui uma classe auxiliar sem fio do IHV que se conecta ao NDF e pode diagnosticar problemas de conectividade relacionados às extensões sem fio ou de segurança do RNWF. As classes auxiliares de diagnóstico de WLAN da MS consultarão essa ID do serviço de configuração automática sem fio quando os módulos IHV forem instalados e fornecerão essa ID como a referência ou o atributo correspondente ao NDF durante uma sessão de diagnóstico para que o NDF possa chamar a classe auxiliar sem fio de terceiros apropriada quando necessário.

**\[Cadeia de \_ caracteres de GUID diagnosticsid \_\]**

Esse valor deve ser uma cadeia de caracteres com todas as letras maiúsculas. Por exemplo, "{12345678-9ABC-DEF0-1234-56789ABCDEF0}".

## <a name="scope-of-80211-wireless-diagnostics-helper-classes"></a>Escopo de classes auxiliares de diagnóstico sem fio 802,11

802,11 classes auxiliares de diagnóstico sem fio atualmente diagnosticam problemas sem fio nas áreas a seguir.

-   Quaisquer problemas de conectividade de 802,11, incluindo a associação de 802,11, a autenticação 802,11, as configurações de segurança 802,11 relacionadas aos padrões do 802,11 & protocolos com suporte nativo no sistema operacional e problemas de desempenho.
-   problemas de segurança de camada 2 com relação a configurações 802.1 x e quaisquer problemas relacionados à autenticação de camada 2 usando métodos com suporte nativo no Windows Vista e no Windows Server 2008.
-   Incompatibilidades de configuração nas configurações de perfil entre o cliente e o ponto de acesso ou a infraestrutura de rede e serviços.

as classes auxiliares de diagnóstico sem fio 802,11 atualmente não diagnosticam problemas sem fio nas áreas a seguir.

-   Problemas relacionados a extensões 802,11 de terceiros, incluindo quaisquer configurações de perfil ou driver relacionadas a essas extensões.
-   Problemas relacionados a métodos EAP de terceiros.
-   Problemas do driver de miniporta sem fio.
-   Qualquer protocolo de segurança 802,11 e camada 2 ou problemas relacionados a padrões que não têm suporte nativo.
-   Problemas no nível do sistema ou do componente que podem afetar a conectividade sem fio, como gerenciamento de energia, pouco espaço em disco, condições de memória e problemas de hardware.

Além disso, 802,11 o diagnóstico sem fio não analisa casos [**highutilization dos**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-highutilization) . Os problemas de desempenho sem fio identificados serão analisados e relatados como casos [**LowHealth**](/windows/desktop/api/ndhelper/nf-ndhelper-inetdiaghelper-lowhealth) .

 

 




