---
description: Descreve a instalação local do WMI.
ms.assetid: 907b65b2-a853-40f4-8b36-5a05a2b1cf85
ms.tgt_platform: multiple
title: Classe __CIMOMIdentification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __CIMOMIdentification
- Root.__CIMOMIdentification.SetupDateTime
- Root.__CIMOMIdentification.VersionCurrentlyRunning
- Root.__CIMOMIdentification.VersionUsedToCreateDB
- Root.__CIMOMIdentification.WorkingDirectory
api_type:
- Schema
api_location:
- Root
ms.openlocfilehash: a8590a2a83cdbc9bd06575cf17ddbe65138a4a31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765710"
---
# <a name="__cimomidentification-class"></a>\_\_Classe CIMOMIdentification

A classe de sistema **\_ \_ CIMOMIdentification** descreve a instalação local do WMI. Essa é uma classe singleton; Há apenas uma instância. A classe **\_ \_ CIMOMIdentification** está disponível apenas nos namespaces **raiz** e **raiz \\ padrão** . Os usuários consultam a instância para obter informações sobre a instalação do WMI.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[singleton]
class __CIMOMIdentification : __SystemClass
{
  string SetupDateTime;
  string VersionCurrentlyRunning;
  string VersionUsedToCreateDB;
  string WorkingDirectory;
};
```

## <a name="members"></a>Membros

A classe **\_ \_ CIMOMIdentification** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **\_ \_ CIMOMIdentification** tem essas propriedades.

<dl> <dt>

**Setupdatetime**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Data e hora da instalação. Essa propriedade estará vazia depois que o sistema operacional for instalado pela primeira vez.

Se o repositório WMI tiver sido excluído e, em seguida, criado novamente, essa propriedade conterá a data e a hora em que o repositório será criado novamente.

</dd> <dt>

**VersionCurrentlyRunning**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica a versão da imagem real que contém o serviço WMI que criou o repositório modelo CIM (CIM). Como o formato do repositório pode ser alterado entre as versões do WMI, essa propriedade permite atualizações futuras do WMI para determinar se o banco de dados deve ser atualizado. O formato é:

"1.00.183.0000"

onde o primeiro dígito é a versão principal, os próximos dois dígitos são versões secundárias e os três próximos dígitos são o número da versão. Os dígitos restantes não são usados.

</dd> <dt>

**VersionUsedToCreateDB**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica a versão da imagem real que contém o serviço WMI que criou o repositório CIM. Como o formato do repositório pode ser alterado entre as versões do WMI, essa propriedade permite atualizações futuras do WMI para determinar se o banco de dados deve ser atualizado. O formato é:

"1.00.183.0000"

onde o primeiro dígito é a versão principal, os próximos dois dígitos são versões secundárias e os três próximos dígitos são o número da versão. Os dígitos restantes não são usados.

</dd> <dt>

**WorkingDirectory**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Diretório de instalação.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **\_ \_ CIMOMIdentification** é derivada de [**\_ \_ SystemClass**](--systemclass.md), que não tem propriedades.

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir descreve como exibir informações de identificação do modelo de objeto CIM e foi tirado do diretório de exemplo em \\ \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Sysmgmt \\ WMI \\ scripting.


```VB
on error resume next 
set cimomid = GetObject("winmgmts:root\default:__cimomidentification=@")

if err <> 0 then
 WScript.Echo ErrNumber, Err.Source, Err.Description
else
 WScript.Echo cimomid.path_.displayname
 WScript.Echo cimomid.versionusedtocreatedb
end if
```



O exemplo de código Perl a seguir descreve como exibir informações de identificação do modelo de objeto CIM e foi tirado do diretório de exemplo em \\ \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ Samples \\ Sysmgmt \\ WMI \\ scripting.


```Perl
use strict;
use Win32::OLE;

my ($Cimomid, $locator, $services);

eval { $Cimomid = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default")->
 Get("__CIMOMIdentification=@"); };

unless ($@)
{
 print "\n", $Cimomid->Path_()->{displayname}, "\n";
 print $Cimomid->{versionusedtocreatedb}, "\n";
}
else
{ 
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Root<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[Classes do sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

