---
description: O provedor SNMP dá suporte à escrita em arquivos de log e no depurador.
ms.assetid: 66627927-2eee-4d56-a74b-f86147ad7711
ms.tgt_platform: multiple
title: Eventos SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 925ce6bb5eca0a3c067470255296ba6c9f66c0183b2b74aa6cfa4a25824446d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816642"
---
# <a name="snmp-events"></a>Eventos SNMP

O provedor SNMP dá suporte à escrita em arquivos de log e no depurador.

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Um número de chaves e valores do Registro define o nível e o tipo de registro em log que está sendo gerado no momento:

-   Depuração

    A chave do Registro de LOG DE PROVEDORES DE **\_ \_ \\ \\ \\ WBEM \\ \\** DO MICROSOFT HKEY LOCAL MACHINE SOFTWARE CONTÉM o valor de log que indica se as informações podem ser escritas no depurador. O valor de log é definido como 0 para desabilitar a saída de depuração ou 1 para habilita-la. O registro em log é um \_ valor REG DWORD.

-   Registro em log

    A chave do registro **\_ \_ \\ \\ \\ \\ WBEM PROVIDERS LOGGING \\ \\ WBEMSNMP** do SOFTWARE DE COMPUTADOR LOCAL HKEY contém todas as informações de log específicas para o provedor SNMP. A tabela a seguir lista os valores associados a essa chave.



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
<td><strong>REG_SZ</strong><br/> Aceita um dos seguintes valores:<br/> &quot;Arquivo &quot; = (Padrão) Envia a saída de depuração para um arquivo.<br/> &quot;Depurador &quot; = Envia a saída de depuração para o depurador.<br/></td>
</tr>
<tr class="even">
<td>MaxFileSize</td>
<td><strong>REG_DWORD</strong><br/> Aceita valores inteiros de 1024 a 2^32-1. O valor é o tamanho máximo permitido em bytes para o arquivo de log. Se for menor que 1024, o mecanismo de registro em log usará um valor de 1024. Um tamanho mínimo de 8 KB é recomendado para esse valor. Quando o arquivo atinge o tamanho especificado por MaxFileSize, o nome do arquivo é anexado com um caractere '~' e um novo arquivo é criado. Portanto, o espaço em disco máximo necessário para o registro em log é duas vezes esse valor.<br/></td>
</tr>
<tr class="odd">
<td>Arquivo</td>
<td><strong>REG_SZ</strong><br/> Define o nome do arquivo para o qual a saída de depuração é enviada quando o tipo de log é definido como 'File'. O valor padrão é ' <WBEMLOGS> \wbemsnmp.log.' Se o diretório não puder ser determinado na seção registro WMI, o valor será <WBEMLOGS> 'c:\wbemsnmp.log'. Se um compartilhamento for usado, como \\ machine\share\wbemsnmp.log ou M:\wbemsnmp.log em que M: é machine\share, a conta system local na qual o WMI é executado deve ter direitos de acesso de leitura/gravação para o \\ \\ computador\compartilhamento.<br/></td>
</tr>
<tr class="even">
<td>Nível</td>
<td><strong>REG_DWORD</strong><br/> Aceita valores inteiros de 0 a 2^32-1. O valor é uma máscara lógica que consiste em 32 bits. As máscaras de bits a seguir são combinadas para definir o tipo de saída de depuração gerada:<br/>
<ul>
<li>0: Invocações de método <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> do provedor de classe SNMP</li>
<li>1: Implementação do provedor de classe SNMP</li>
<li>2: Invocações de método <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> do provedor de instância SNMP</li>
<li>3: Implementação do provedor de instância SNMP</li>
<li>4: Biblioteca de classes SNMP</li>
<li>5: SNMP SMIR</li>
<li>6: Correlator SNMP</li>
<li>7: Código de mapeamento de tipo SNMP</li>
<li>8: Código de threading SNMP</li>
<li>9: Interfaces e implementação do provedor de eventos SNMP</li>
</ul>
Delimita Nível como (2^0 + 2^8=) 257 para operações que envolvem chamadas para os métodos <a href="/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices"><strong>IWbemServices</strong></a> do provedor de classe SNMP e operações usando o código de threading SNMP.<br/></td>
</tr>
</tbody>
</table>



 

 

 




