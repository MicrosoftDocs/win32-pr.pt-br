---
description: Conceitualmente semelhante a um Uniform Resource Locator (URL), um caminho de objeto WMI é uma cadeia de caracteres que identifica exclusivamente o namespace em um servidor, uma classe dentro de um namespace ou instâncias de uma classe.
ms.assetid: 7a390541-609d-4b97-b91c-1a41d21ec17d
ms.tgt_platform: multiple
title: Descrevendo o local de um objeto WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b58b58a6b668955d6eba1e4c51f6f8dccdac890
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787783"
---
# <a name="describing-the-location-of-a-wmi-object"></a>Descrevendo o local de um objeto WMI

Conceitualmente semelhante a um Uniform Resource Locator (URL), um caminho de objeto WMI é uma cadeia de caracteres que identifica exclusivamente o namespace em um servidor, uma classe dentro de um namespace ou instâncias de uma classe. Um caminho de objeto é hierárquico e contém vários elementos que descrevem o local do objeto em questão. Assim como os caminhos de arquivo, os caminhos de objeto do WMI podem ser descritos em completo ou especificado como um caminho relativo.

O namespace de um objeto WMI é listado na página de referência do WMI. Por exemplo, o local da maioria das classes com suporte nos [provedores WMI CIMWin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers) está localizado no \\ \\ namespace raiz cimv2. O código do PowerShell a seguir descreve uma chamada para recuperar o objeto de [**\_ ComputerSystem do Win32**](/windows/desktop/CIMWin32Prov/win32-computersystem) em seu computador local:

`Get-WmiObject -Class Win32_ComputerSystem -Namespace "root\cimv2" -ComputerName "."`

Como alternativa, uma instância específica do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) pode ter o seguinte caminho da propriedade [**SWbemObject. \_ Path**](swbemobject-path-.md) .

`\\Machine1\root\cimv2:Win32_LogicalDisk.DeviceID="C:"`

O exemplo a seguir mostra o caminho relativo para essa instância, como visto exibindo a propriedade [**RelPath**](swbemobjectpath-relpath.md) do objeto [**SWbemObjectPath**](swbemobjectpath.md) retornado pela chamada para [**SWbemObject. Path \_**](swbemobject-path-.md).

`Win32_LogicalDisk.DeviceID="A:"`

Observe que **DeviceID** é a propriedade de chave da classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .

## <a name="c"></a>C++

A tabela a seguir lista os tipos de caminho de objeto e os métodos associados que exigem caminhos de objeto.



<table>
<thead>
<tr class="header">
<th>Tipo de caminho do objeto</th>
<th>Método</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="describing-a-wmi-namespace-object-path.md">Namespace</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace"><strong>IWbemServices:: OpenNamespace</strong></a><br />
</dl></td>
</tr>
<tr class="even">
<td><a href="describing-a-class-object-path.md">Classe</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod"><strong>IWbemServices:: ExecMethod</strong></a><br />
[<strong>IWbemServices:: ExecMethodAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="describing-a-class-object-path.md">Classe</a> ou <a href="describing-an-instance-object-path.md">instância</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject"><strong>IWbemServices:: GetObject</strong></a><br />
[<strong>IWbemServices:: GetObjectAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="describing-an-instance-object-path.md">Instância</a></td>
<td><dl><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance"><strong>IWbemServices::D eleteInstance</strong></a><br />
[<strong>IWbemServices::D eleteinstanceasync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)<br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="script"></a>Script

Os caminhos de objeto podem ser construídos de várias maneiras:

-   Recupere a propriedade de um método que retorna um objeto [**SWbemObjectPath**](swbemobjectpath.md) .
-   Recupere a propriedade [**SWbemObject. \_ Path**](swbemobject-path-.md) .
-   Crie uma variável de cadeia de caracteres que contenha o caminho do objeto.

A tabela a seguir lista os objetos de script que exigem caminhos de objeto.



<table>
<thead>
<tr class="header">
<th>Objeto de script</th>
<th>Método</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="swbemservices.md"><strong>SWbemServices</strong></a></td>
<td><dl><a href="swbemservices-associatorsof.md"><strong>AssociatorsOf</strong></a><br />
[<strong>AssociatorsOfAsync</strong>] (swbemservices-associatorsofasync.md)<br />
[<strong>Excluir</strong>] (swbemservices-delete.md)<br />
[<strong>DeleteAsync</strong>] (swbemservices-deleteasync.md)<br />
[<strong>ExecMethod</strong>] (swbemservices-execmethod.md)<br />
[<strong>ExecMethodAsync</strong>] (swbemservices-execmethodasync.md)<br />
[<strong>Obter</strong>] (swbemservices-get.md)<br />
[<strong>Getasync</strong>] (swbemservices-getasync.md)<br />
[<strong>ReferenceTo</strong>] (swbemservices-referencesto.md)<br />
[<strong>ReferencesToAsync</strong>] (swbemservices-referencestoasync.md)<br />
</dl></td>
</tr>
<tr class="even">
<td><a href="swbemobjectset.md"><strong>SWbemObjectSet</strong></a></td>
<td><dl><a href="swbemobjectset-item.md"><strong>Item</strong></a><br />
</dl></td>
</tr>
</tbody>
</table>



 

 

 
