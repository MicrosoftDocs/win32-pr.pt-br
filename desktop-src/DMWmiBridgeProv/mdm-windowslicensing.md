---
title: Classe MDM_WindowsLicensing
description: A \_ classe MDM WindowsLicensing foi projetada para cenários de gerenciamento relacionados ao licenciamento.
ms.assetid: 9b26d8dc-aab6-4c67-9dbc-4b53525b9354
keywords:
- Classe MDM_WindowsLicensing
- Classe MDM_WindowsLicensing, descrita
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing
- MDM_WindowsLicensing.InstanceID
- MDM_WindowsLicensing.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd77bbdb1a7e5c708ebcd955a0c8854c7c7404b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105771688"
---
# <a name="mdm_windowslicensing-class"></a>\_Classe WindowsLicensing do MDM

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

A classe **MDM \_ WindowsLicensing** foi projetada para cenários de gerenciamento relacionados ao licenciamento. Atualmente, o escopo é limitado a atualizações de edição de dispositivos Windows 10 desktop e Mobile, como Windows 10 pro para Windows 10 Enterprise. Além disso, esse CSP fornece a capacidade de ativar ou alterar a chave do produto de dispositivos Windows 10 desktop.

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_WindowsLicensing
{
  string InstanceID;
  string ParentID;
  sint32 Edition;
  sint32 Status;
  string LicenseKeyType;
};
```

## <a name="members"></a>Membros

A classe **MDM \_ WindowsLicensing** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **MDM \_ WindowsLicensing** tem esses métodos.



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
<td style="text-align: left;"><a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>ChangeProductKeyMethod</strong></a></td>
<td style="text-align: left;">Instala uma chave do produto para dispositivos Windows 10 desktop. Não reinicia.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>CheckApplicabilityMethod</strong></a></td>
<td style="text-align: left;">Para verificar se a chave do produto (Product Key) inserida pode ser usada para uma atualização de edição, ativar ou alterar uma chave de produto do Windows 10 para dispositivos de desktop.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>UpgradeEditionWithLicenseMethod</strong></a></td>
<td style="text-align: left;">Forneça uma licença para uma atualização de edição de dispositivos Windows 10 Mobile.<br/>
<blockquote>
[!Note]<br />
Esse processo de atualização não exige uma reinicialização do sistema.
</blockquote>
<br/> <br/> O tipo de data é XML.<br/> A operação com suporte é executada.<br/>
<blockquote>
[!Important]<br />
O conteúdo do arquivo de licença XML deve ter um escape adequado (ou seja, não deve simplesmente ser um XML copiado), caso contrário, a atualização de edição em dispositivos Windows 10 Mobile falhará. Para obter mais informações sobre a saída correta do arquivo de licença XML, consulte a seção 2,4 da <a href="https://www.w3.org/TR/xml/">especificação XML do W3C</a>. O arquivo de licença XML é adquirido do centro de serviços de licenciamento por volume da Microsoft. Sua organização deve ter um contrato de licenciamento por volume com a Microsoft para acessar o Portal.
</blockquote>
<br/> Estes são os caminhos de atualização de edição válidos ao usar este nó por meio de um pacote MDM ou de provisionamento:
<ul>
<li>Windows 10 Mobile para Windows 10 Mobile Enterprise<br/></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>UpgradeEditionWithProductKeyMethod</strong></a></td>
<td style="text-align: left;">Dispara o dispositivo para pegar a chave do produto e atualizar a edição do cliente.
<blockquote>
[!Note]<br />
Esse processo de atualização requer uma reinicialização do sistema.
</blockquote>
<br/> <br/> A operação com suporte é executada.<br/> Quando uma chave do produto é enviada por push de um servidor MDM para um dispositivo do usuário, o <strong>changepk.exe</strong> é executado usando a chave do produto. Após a conclusão, uma notificação é mostrada ao usuário de que uma nova edição do Windows 10 está disponível. O usuário pode reiniciar o sistema manualmente ou, após duas horas, o dispositivo será reiniciado automaticamente para concluir a atualização. O usuário receberá uma notificação de lembrete 10 minutos antes da reinicialização automática.<br/> Depois que o dispositivo for reiniciado, o processo de upgrade de edição será reiniciado. O usuário receberá uma notificação de upgrade bem-sucedido.
<blockquote>
[!Important]<br />
Se outra política exigir uma reinicialização do sistema que ocorra quando <strong>changepk.exe</strong> estiver em execução, a atualização da edição falhará.
</blockquote>
<br/> <br/> Se uma chave do produto (Product Key) for inserida em um pacote de provisionamento e o usuário iniciar a instalação do pacote, uma notificação será mostrada ao usuário dizendo que o sistema será reiniciado para a conclusão da instalação do pacote. Após o consentimento explícito do usuário para continuar, o pacote continua a instalação e <strong>changepk.exe</strong> é executado usando a chave do produto. O usuário receberá uma notificação de lembrete 30 segundos antes do reinício automático. <br/> Depois que o dispositivo for reiniciado, o processo de upgrade de edição será reiniciado. O usuário receberá uma notificação de upgrade bem-sucedido. <br/> Esse nó também pode ser usado para ativar ou alterar uma chave do produto (Product Key) em uma edição específica do dispositivo de desktop do Windows 10 inserindo uma chave do produto (Product Key). A ativação ou a alteração de uma chave do produto não requer uma reinicialização e é um processo silencioso para o usuário.<br/>
<blockquote>
[!Important]<br />
A chave do produto (Product Key) inserida deve ter 29 caracteres (ou seja, deve incluir traços), caso contrário, a ativação, a atualização de edição ou a alteração da chave do produto em dispositivos com Windows 10 desktop falharão. A chave do produto é adquirida do centro de serviços de licenciamento por volume da Microsoft. Sua organização deve ter um contrato de licenciamento por volume com a Microsoft para acessar o Portal.
</blockquote>
<br/> Estes são os caminhos de atualização de edição válidos ao usar este nó por meio de um MDM:
<ul>
<li>Windows 10 Enterprise para Windows 10 Education</li>
<li>Windows 10 home to Windows 10 Education</li>
<li>Windows 10 pro para Windows 10 Education</li>
<li>Windows 10 pro para Windows 10 Enterprise</li>
</ul>
<br/> A ativação ou a alteração de uma chave do produto pode ser executada nas seguintes edições:
<ul>
<li>Windows 10 Education</li>
<li>Windows 10 Enterprise</li>
<li>Windows 10 Home</li>
<li>Windows 10 Pro</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Propriedades

A classe **MDM \_ WindowsLicensing** tem essas propriedades.

<dl> <dt>

[Edição](/windows/client-management/mdm/windowslicensing-csp#edition)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
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

[LicenseKeyType](/windows/client-management/mdm/windowslicensing-csp#licensekeytype)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descreve o caminho completo para o nó pai. Para essa classe, a cadeia de caracteres é "./Vendor/MSFT/"

</dd> <dt>

[Status](/windows/client-management/mdm/windowslicensing-csp#subscriptions-subscriptionid-status)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Namespace<br/>                | \\DMMap de \\ MDM \\ CIMv2 raiz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Como usar os scripts do PowerShell com o provedor de ponte WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

