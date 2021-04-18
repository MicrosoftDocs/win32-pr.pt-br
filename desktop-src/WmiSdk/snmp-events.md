---
description: O provedor SNMP dá suporte à gravação em arquivos de log e ao depurador.
ms.assetid: 66627927-2eee-4d56-a74b-f86147ad7711
ms.tgt_platform: multiple
title: Eventos SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94b133d2fc81c76949439b3e1f26d1fc448f0b13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749879"
---
# <a name="snmp-events"></a>Eventos SNMP

O provedor SNMP dá suporte à gravação em arquivos de log e ao depurador.

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

Várias chaves e valores do registro definem o nível e o tipo de log que está sendo gerado no momento:

-   Depuração

    A chave de registro de **log do hKey \_ local \_ Machine \\ software \\ Microsoft \\ WBEM \\ Providers \\** contém o valor de log que indica se as informações podem ser gravadas no depurador. O valor de log é definido como 0 para desabilitar a saída de depuração ou 1 para habilitá-la. Logging é um valor de REG \_ DWORD.

-   Log

    A chave de registro **HKEY \_ local \_ \\ software \\ Microsoft \\ WBEM \\ Providers \\ Logging \\ WBEMSNMP** mantém todas as informações de log específicas para o provedor SNMP. A tabela a seguir lista os valores associados a essa chave.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Type</td>
<td><strong>REG_SZ</strong><br/> Usa um dos seguintes valores:<br/> &quot;File &quot; = (padrão) envia a saída de depuração para um arquivo.<br/> &quot;Debugger &quot; = envia a saída de depuração para o depurador.<br/></td>
</tr>
<tr class="even">
<td>MaxFileSize</td>
<td><strong>REG_DWORD</strong><br/> Obtém valores inteiros de 1024 a 2 ^ 32-1. O valor é o tamanho máximo permitido em bytes para o arquivo de log. Se for menor que 1024, o mecanismo de registro em log usará um valor de 1024. Um tamanho mínimo de 8 KB é recomendado para esse valor. Quando o arquivo atinge o tamanho especificado por MaxFileSize, o nome do arquivo é anexado com um caractere ' ~ ' e um novo arquivo é criado. Portanto, o espaço em disco máximo necessário para o registro em log é o dobro desse valor.<br/></td>
</tr>
<tr class="odd">
<td>Arquivo</td>
<td><strong>REG_SZ</strong><br/> Define o nome do arquivo para o qual a saída de depuração é enviada quando o tipo de log é definido como ' file '. O valor padrão é ' <WBEMLOGS> \wbemsnmp.log. ' Se o <WBEMLOGS> diretório não puder ser determinado na seção do registro WMI, o valor padrão será ' c:\wbemsnmp.log '. Se um compartilhamento for usado, como \\ machine\share\wbemsnmp.log ou M:\wbemsnmp.log, em que M: é \\ machine\share, a conta do sistema local na qual o WMI é executado deve ter direitos de acesso de leitura/gravação para o \\ machine\share.<br/></td>
</tr>
<tr class="even">
<td>Nível</td>
<td><strong>REG_DWORD</strong><br/> Obtém valores inteiros de 0 a 2 ^ 32-1. O valor é uma máscara lógica que consiste em 32 bits. As seguintes máscaras de bits são combinadas para definir o tipo de saída de depuração gerada:<br/>
<ul>
<li>0: invocações do método <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> do provedor de classe SNMP</li>
<li>1: implementação do provedor de classe SNMP</li>
<li>2: invocações do método <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> do provedor de instância SNMP</li>
<li>3: implementação do provedor de instância SNMP</li>
<li>4: biblioteca de classes SNMP</li>
<li>5: SNMP SMIR</li>
<li>6: correlator SNMP</li>
<li>7: código de mapeamento de tipo SNMP</li>
<li>8: código de Threading SNMP</li>
<li>9: interfaces e implementação do provedor de eventos SNMP</li>
</ul>
Defina nível como (2 ^ 0 + 2 ^ 8 =) 257 para operações envolvendo chamadas para os métodos de <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> do provedor de classe SNMP e operações usando o código de Threading SNMP.<br/></td>
</tr>
</tbody>
</table>



 

 

 




