---
title: Classe Win32_RDMSJoinedNode
description: Representa um nó de servidor gerenciado por serviços de gerenciamento de Área de Trabalho Remota (RDMS).
ms.assetid: 8751f3f7-dfb5-45bd-a6b1-758aa22a3569
ms.tgt_platform: multiple
keywords:
- Classe de Win32_RDMSJoinedNode Serviços de Área de Trabalho Remota
- Serviços de Área de Trabalho Remota de Win32_RDMSJoinedNode classe, descrita
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode
- Win32_RDMSJoinedNode.FQDN
- Win32_RDMSJoinedNode.SID
- Win32_RDMSJoinedNode.OSVersion
- Win32_RDMSJoinedNode.IsRdcb
- Win32_RDMSJoinedNode.IsRdg
- Win32_RDMSJoinedNode.IsRdls
- Win32_RDMSJoinedNode.IsRdvh
- Win32_RDMSJoinedNode.IsRdwa
- Win32_RDMSJoinedNode.IsRdsh
- Win32_RDMSJoinedNode.IsWebAccessCertificateInstalled
- Win32_RDMSJoinedNode.IsGatewayCertificateInstalled
- Win32_RDMSJoinedNode.IsRedirectorCertificateInstalled
- Win32_RDMSJoinedNode.IsPublishingCertificateInstalled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cabf1cf7ff98b698624285b2877412c4323259b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369268"
---
# <a name="win32_rdmsjoinednode-class"></a>\_Classe Win32 RDMSJoinedNode

Representa um nó de servidor gerenciado por serviços de gerenciamento de Área de Trabalho Remota (RDMS).

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSJoinedNode
{
  string  FQDN;
  string  SID;
  String  OSVersion;
  boolean IsRdcb;
  boolean IsRdg;
  boolean IsRdls;
  boolean IsRdvh;
  boolean IsRdwa;
  boolean IsRdsh;
  boolean IsWebAccessCertificateInstalled;
  boolean IsGatewayCertificateInstalled;
  boolean IsRedirectorCertificateInstalled;
  boolean IsPublishingCertificateInstalled;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ RDMSJoinedNode** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Win32 \_ RDMSJoinedNode** tem esses métodos.



| Método                                                                | Descrição                                                                                                                                                                                           |
|:----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetJoinedNodeCount**](win32-rdmsjoinednode-getjoinednodecount.md) | **Windows server 2012 R2 e Windows server 2012:** Esse método não está disponível antes do Windows Server 2016.<br/> Obtém o número de servidores que têm a função especificada instalada.<br/> |
| [**Join**](join-win32-rdmsjoinednode.md)                             | Adiciona um nó a RDMS.<br/>                                                                                                                                                                       |
| [**Sair**](unjoin-win32-rdmsjoinednode.md)                         | Remove um nó de RDMS.<br/>                                                                                                                                                                  |



 

### <a name="properties"></a>Propriedades

A classe **Win32 \_ RDMSJoinedNode** tem essas propriedades.

<dl> <dt>

**FQDN**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Obtém o nome de domínio totalmente qualificado do nó.

</dd> <dt>

**IsGatewayCertificateInstalled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Obtém e define um valor que indica se o servidor tem um certificado para executar a autenticação para conexões Área de Trabalho Remota gateway. **True** se o certificado estiver instalado; caso contrário, **false**.

</dd> <dt>

**IsPublishingCertificateInstalled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Obtém e define um valor que indica se o servidor tem um certificado para assinar protocolo RDP arquivos de publicação. **True** se o certificado estiver instalado; caso contrário, **false**.

</dd> <dt>

**IsRdcb**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Obtém e define um valor que indica se o servidor está Conexão de Área de Trabalho Remota Agente. **True** se o servidor for um agente de conexão de área de trabalho remota; caso contrário, **false**.

</dd> <dt>

**IsRdg**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Obtém e define um valor que indica se o servidor está Área de Trabalho Remota servidor de gateway. **True** se o servidor for um servidor de gateway área de trabalho remota; caso contrário, **false**.

</dd> <dt>

**IsRdls**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Obtém e define um valor que indica se o servidor está Área de Trabalho Remota servidor de licença. **True** se o servidor for um servidor de licença área de trabalho remota; caso contrário, **false**.

</dd> <dt>

**IsRdsh**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Obtém e define um valor que indica se o servidor está Área de Trabalho Remota servidor host de sessão. **True** se o servidor for um servidor host de sessão área de trabalho remota; caso contrário, **false**.

</dd> <dt>

**IsRdvh**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Obtém e define um valor que indica se o servidor está Área de Trabalho Remota host de virtualização. **True** se o servidor for um host de virtualização área de trabalho remota; caso contrário, **false**.

</dd> <dt>

**IsRdwa**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Obtém e define um valor que indica se o servidor é Área de Trabalho Remota servidor de acesso à Web. **True** se o servidor for um servidor de acesso via Web à área de trabalho remota; caso contrário, **false**.

</dd> <dt>

**IsRedirectorCertificateInstalled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Obtém e define um valor que indica se o servidor tem um certificado para executar a autenticação para Serviços de Área de Trabalho Remota implantação. **True** se o certificado estiver instalado; caso contrário, **false**.

</dd> <dt>

**IsWebAccessCertificateInstalled**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Obtém e define um valor que indica se o servidor tem um certificado para executar a autenticação para Acesso via Web à Área de Trabalho Remota. **True** se o certificado estiver instalado; caso contrário, **false**.

</dd> <dt>

**OSVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Obtém e define a versão dos sistemas operacionais no nó.

</dd> <dt>

**SID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Obtém o identificador de segurança (SID) do nó.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\RDMs cimv2 \\ raiz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Provedor de serviços de gerenciamento de Área de Trabalho Remota](rdms-api-reference.md)
</dt> </dl>

 

