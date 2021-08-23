---
title: MDM_VPNv2_RouteList02_01 classe
description: A classe MDM \_ VPNv2 \_ RouteList02 01 contém uma lista opcional de rotas a serem adicionadas à tabela de roteamento para \_ a interface VPN.
ms.assetid: 4271b0c4-9d29-4148-b956-ac9306316c9b
keywords:
- MDM_VPNv2_RouteList02_01 classe
- MDM_VPNv2_RouteList02_01 classe, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_RouteList02_01
- MDM_VPNv2_RouteList02_01.InstanceID
- MDM_VPNv2_RouteList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14ea9725d70d3acfe4e6831d1d386aedecfd9374728b103d50b67aa15cb61ec9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750266"
---
# <a name="mdm_vpnv2_routelist02_01-class"></a>Classe MDM \_ VPNv2 \_ RouteList02 \_ 01

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

A **classe MDM \_ VPNv2 \_ RouteList02 \_ 01** contém uma lista opcional de rotas a serem adicionadas à tabela de roteamento para a interface VPN.

Isso é necessário para o caso de túnel dividido em que o site do servidor VPN tem mais sub-redes que a sub-rede padrão com base no IP atribuído à interface.

Cada computador que executa TCP/IP toma decisões de roteamento. Essas decisões são controladas pela tabela de roteamento de IP. Adicionar valores nesse nó atualiza a tabela de roteamento com rotas para a interface VPN após a conexão. Os valores nesse nó representam o prefixo de destino das rotas IP. Um prefixo de destino consiste em um prefixo de endereço IP e um comprimento de prefixo.

Adicionar uma rota aqui permite que a pilha de rede identifique o tráfego que precisa passar pela interface VPN para VPN de túnel dividido. Alguns servidores VPN podem configurar isso durante a negociação de conexão e não precisam dessa informação no Perfil de VPN. Verifique com o administrador do servidor VPN para determinar se você precisa das informações no perfil de VPN.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_RouteList02_01
{
  string InstanceID;
  string ParentID;
  string Address;
  sint32 PrefixSize;
};
```

## <a name="members"></a>Membros

A **classe MDM \_ VPNv2 \_ RouteList02 \_ 01** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe MDM \_ VPNv2 \_ RouteList02 \_ 01** tem essas propriedades.

<dl> <dt>

[Endereço](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-address)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica o nome do nó pai.

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descreve o caminho completo para o nó pai. Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/VPNv2/*ProfileName*/RouteList"

</dd> <dt>

[PrefixSize](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-routelist-routerowid-prefixsize)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Namespace<br/>                | \\Cimv2 \\ mdm \\ dmmap raiz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Como usar os scripts do PowerShell com o provedor de ponte WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

