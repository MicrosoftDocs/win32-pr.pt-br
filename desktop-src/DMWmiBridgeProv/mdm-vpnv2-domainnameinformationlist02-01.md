---
title: Classe MDM_VPNv2_DomainNameInformationList02_01
description: A \_ classe MDM VPNv2 \_ DomainNameInformationList02 \_ 01 descreve as regras de tabela de políticas de resolução de nomes (NRPT) para o perfil VPN.
ms.assetid: ed6863aa-f85e-4f65-9312-ddf60a8c0d5a
keywords:
- Classe MDM_VPNv2_DomainNameInformationList02_01
- Classe MDM_VPNv2_DomainNameInformationList02_01, descrita
topic_type:
- apiref
api_name:
- MDM_VPNv2_DomainNameInformationList02_01
- MDM_VPNv2_DomainNameInformationList02_01.InstanceID
- MDM_VPNv2_DomainNameInformationList02_01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8728f7a0e781f3cbd74c1783fd1ba388121232e41c7054c4515db64ece977d7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045576"
---
# <a name="mdm_vpnv2_domainnameinformationlist02_01-class"></a>\_Classe MDM VPNv2 \_ DomainNameInformationList02 \_ 01

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

A classe **MDM \_ VPNv2 \_ DomainNameInformationList02 \_ 01** descreve as regras de tabela de políticas de resolução de nomes (NRPT) para o perfil VPN.

a Tabela de Políticas de Resolução de Nomes (NRPT) é uma tabela de namespaces e configurações correspondentes armazenadas no registro de Windows que determina o comportamento do cliente DNS ao emitir consultas e processar respostas. Cada linha na NRPT representa uma regra para uma parte do namespace para o qual o cliente DNS emite consultas. Antes de emitir consultas de resolução de nomes, o cliente DNS consulta a NRPT para determinar se qualquer sinalizador adicional deve ser definido na consulta. Depois de receber a resposta, o cliente consultará novamente o NRPT para verificar se há algum requisito especial de processamento ou política. Na ausência da NRPT, o cliente opera com base nos servidores DNS e nos sufixos definidos na interface.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system", "local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_VPNv2_DomainNameInformationList02_01
{
  string InstanceID;
  string ParentID;
  string DomainName;
  string DomainNameType;
  string DnsServers;
  string WebProxyServers;
};
```

## <a name="members"></a>Membros

A classe **MDM \_ VPNv2 \_ DomainNameInformationList02 \_ 01** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **MDM \_ VPNv2 \_ DomainNameInformationList02 \_ 01** tem essas propriedades.

<dl> <dt>

[DnsServers](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-dnsservers)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[DomainName](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-domainname)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

[DomainNameType](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-domainnametype)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
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

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descreve o caminho completo para o nó pai. Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/VPNv2/*ProfileName*"

</dd> <dt>

[WebProxyServers](/windows/client-management/mdm/vpnv2-csp#vpnv2-profilename-domainnameinformationlist-dnirowid-webproxyservers)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Namespace<br/>                | \\Dmmap de \\ MDM \\ cimv2 raiz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Como usar os scripts do PowerShell com o provedor de ponte WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

