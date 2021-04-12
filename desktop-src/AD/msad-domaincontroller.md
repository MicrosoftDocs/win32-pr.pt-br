---
title: Classe MSAD_DomainController
description: Representa o controlador de domínio (DC) no qual o provedor WMI está em execução.
ms.assetid: a7671967-79d7-48f8-8869-dd65272e2ed2
ms.tgt_platform: multiple
keywords:
- Classe de MSAD_DomainController Active Directory
- Active Directory de MSAD_DomainController classe, descrita
topic_type:
- apiref
api_name:
- MSAD_DomainController
- MSAD_DomainController.DistinguishedName
- MSAD_DomainController.CommonName
- MSAD_DomainController.SiteName
- MSAD_DomainController.NTDsaGUID
- MSAD_DomainController.IsGC
- MSAD_DomainController.TimeOfOldestReplSync
- MSAD_DomainController.TimeOfOldestReplAdd
- MSAD_DomainController.TimeOfOldestReplDel
- MSAD_DomainController.TimeOfOldestReplMod
- MSAD_DomainController.TimeOfOldestReplUpdRefs
- MSAD_DomainController.IsNextRIDPoolAvailable
- MSAD_DomainController.PercentOfRIDsLeft
- MSAD_DomainController.IsRegisteredInDNS
- MSAD_DomainController.IsAdvertisingToLocator
- MSAD_DomainController.IsSysVolReady
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303071d3d268953687bc387709c74531f8b40584
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455190"
---
# <a name="msad_domaincontroller-class"></a>\_Classe DOMAINCONTROLLER MSAD

Representa o controlador de domínio (DC) no qual o provedor WMI está em execução.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("ReplProv1")]
class  MSAD_DomainController
{
  String   DistinguishedName;
  String   CommonName;
  String   SiteName;
  String   NTDsaGUID;
  boolean  IsGC = FALSE;
  datetime TimeOfOldestReplSync;
  datetime TimeOfOldestReplAdd;
  datetime TimeOfOldestReplDel;
  datetime TimeOfOldestReplMod;
  datetime TimeOfOldestReplUpdRefs;
  boolean  IsNextRIDPoolAvailable = FALSE;
  uint32   PercentOfRIDsLeft;
  boolean  IsRegisteredInDNS;
  boolean  IsAdvertisingToLocator = FALSE;
  boolean  IsSysVolReady = FALSE;
};
```

## <a name="members"></a>Membros

A **classe \_ DomainController MSAD** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ DomainController MSAD** tem esses métodos.



| Método                                                 | Descrição                                                                              |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**ExecuteKCC**](executekcc-msad-domaincontroller.md) | Invoca o Knowledge Consistency Checker para verificar a topologia de replicação.<br/> |



 

### <a name="properties"></a>Propriedades

A **classe \_ DomainController MSAD** tem essas propriedades.

<dl> <dt>

**CommonName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o nome comum do objeto de servidor.

</dd> <dt>

**DistinguishedName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtém o caminho X. 500 do objeto [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) .

</dd> <dt>

**IsAdvertisingToLocator**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o valor que indica se o serviço localizador no controlador de domínio está anunciando corretamente. **True** se o serviço localizador no controlador de domínio estiver anunciando corretamente; caso contrário, **false**.

</dd> <dt>

**IsGC**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o valor que indica se o DC é um servidor de catálogo global. **True** se o DC for um servidor de catálogo global; caso contrário, **false**.

</dd> <dt>

**IsNextRIDPoolAvailable**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o valor que indica se o controlador de domínio obteve outro pool de RIDs. **True** se o controlador de domínio tiver obtido outro pool de RID e a alocação de RIDs nesse controlador de domínio poderá continuar mesmo se o pool atual de RIDs for esgotado; caso contrário, **false**.

</dd> <dt>

**IsRegisteredInDNS**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o valor que indica se o DC está registrado corretamente no DNS. **True** se o controlador de domínio estiver registrado corretamente no DNS; caso contrário, **false**.

</dd> <dt>

**IsSysVolReady**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o valor que indica se o SysVol foi publicado corretamente. **True** se o SYSVOL tiver sido publicado corretamente; caso contrário, **false**.

</dd> <dt>

**NTDsaGUID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o GUID que está associado ao objeto [**NTDS-DSA**](/windows/desktop/ADSchema/c-ntdsdsa) no contêiner de configuração. O objeto **NTDS-DSA** representa o domínio do Active Directory processo DSA do serviço no servidor.

</dd> <dt>

**PercentOfRIDsLeft**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém a porcentagem de RIDs que são deixados no pool RID atual neste controlador de domínio.

</dd> <dt>

**SiteName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o site no qual o DC existe.

</dd> <dt>

**TimeOfOldestReplAdd**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o carimbo de data/hora da operação de adição de replicação mais antiga que ainda está na fila neste controlador de domínio.

</dd> <dt>

**TimeOfOldestReplDel**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o carimbo de data/hora da operação de exclusão de replicação mais antiga que ainda está na fila neste controlador de domínio.

</dd> <dt>

**TimeOfOldestReplMod**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o carimbo de data/hora da operação de modificação de replicação mais antiga que ainda está na fila neste controlador de domínio.

</dd> <dt>

**TimeOfOldestReplSync**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o carimbo de data/hora da operação de sincronização de replicação mais antiga que ainda está na fila neste controlador de domínio.

</dd> <dt>

**TimeOfOldestReplUpdRefs**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Obtém o carimbo de data/hora da operação de atualização de replicação mais antiga que ainda está na fila neste controlador de domínio.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\MicrosoftActiveDirectory raiz<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

