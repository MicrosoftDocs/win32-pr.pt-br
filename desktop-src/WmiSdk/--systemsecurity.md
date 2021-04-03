---
description: Contém métodos que permitem que você acesse e modifique as configurações de segurança para um namespace.
ms.assetid: a54fdd85-feb8-4727-9f26-fe4f213cab6b
ms.tgt_platform: multiple
title: Classe __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 58de990b56518550705cda2f8360cd90a0381c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091838"
---
# <a name="__systemsecurity-class"></a>\_\_Classe SystemSecurity

A classe de sistema **\_ \_ SystemSecurity** contém métodos que permitem que você acesse e modifique as configurações de segurança de um namespace. A classe **\_ \_ SystemSecurity** é uma classe singleton em cada namespace.

> [!Note]  
> Para obter mais informações, consulte [Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class __SystemSecurity
{
};
```

## <a name="members"></a>Membros

A classe **\_ \_ SystemSecurity** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A classe **\_ \_ SystemSecurity** tem esses métodos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Método</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="--systemsecurity-get9xuserlist.md"><strong>Get9XUserList</strong></a></td>
<td style="text-align: left;">Obtém uma lista de usuários que têm permissão de acesso remoto.<br/>
<blockquote>
[!Note]<br />
Esse método não funciona em versões do Windows com suporte. Em vez disso, use <a href="--systemsecurity-getsd.md"><strong>gets</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="--systemsecurity-getcalleraccessrights.md"><strong>GetCallerAccessRights</strong></a></td>
<td style="text-align: left;">Retorna uma máscara com cada bit que corresponde a um direito de acesso.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="--systemsecurity-getsd.md"><strong>GetSD</strong></a></td>
<td style="text-align: left;">Obtém o <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> para o namespace ao qual o usuário está conectado.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="getsecuritydescriptor-method-in-class---systemsecurity-.md"><strong>GetSecurityDescriptor</strong></a></td>
<td style="text-align: left;">Obtém o descritor de segurança que controla o acesso ao namespace do WMI associado à instância do <strong>__SystemSecurity</strong>. O descritor de segurança é retornado como uma instância de<a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="--systemsecurity-set9xuserlist.md"><strong>Set9XUserList</strong></a></td>
<td style="text-align: left;">Define uma lista de usuários que têm permissão de acesso remoto.<br/>
<blockquote>
[!Note]<br />
Esse método não funciona em versões do Windows com suporte. Em vez disso, use <a href="--systemsecurity-setsd.md"><strong>sets</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="--systemsecurity-setsd.md"><strong>SetSD</strong></a></td>
<td style="text-align: left;">Define o descritor de segurança para o namespace ao qual o usuário está conectado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="setsecuritydescriptor-method-in-class---systemsecurity.md"><strong>SetSecurityDescriptor</strong></a></td>
<td style="text-align: left;">Grava uma versão atualizada do descritor de segurança que controla o acesso à impressora. O descritor de segurança é representado por uma instância do <a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Você pode exigir que os scripts e aplicativos de cliente usem uma conexão criptografada para autenticação adicionando o qualificador **RequiresEncryption** ao arquivo. MOF que cria o namespace. Você também pode modificar um namespace existente adicionando esse atributo e compilar o arquivo. mof novamente. Para obter mais informações sobre como usar o **RequiresEncryption**, consulte [exigindo uma conexão criptografada para um namespace](requiring-an-encrypted-connection-to-a-namespace.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Todos os namespaces do WMI<br/>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Constantes de segurança do WMI](wmi-security-constants.md)
</dt> <dt>

[Objetos do descritor de segurança do WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Protegendo namespaces WMI](securing-wmi-namespaces.md)
</dt> <dt>

[Estabelecendo a herança da segurança do namespace](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[ACLs (listas de controle de acesso)](/windows/desktop/SecAuthZ/access-control-lists)
</dt> <dt>

[**\_Descritor de segurança**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

