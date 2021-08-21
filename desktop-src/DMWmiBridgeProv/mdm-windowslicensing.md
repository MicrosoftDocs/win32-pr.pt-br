---
title: MDM_WindowsLicensing classe
description: A classe MDM \_ WindowsLicensing foi projetada para cenários de gerenciamento relacionados ao licenciamento.
ms.assetid: 9b26d8dc-aab6-4c67-9dbc-4b53525b9354
keywords:
- MDM_WindowsLicensing classe
- MDM_WindowsLicensing classe, descrita
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
ms.openlocfilehash: c2c82b9cb06f7fa141100856bac86aaf6afe1635721a224603b4e78e51fe335f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118164202"
---
# <a name="mdm_windowslicensing-class"></a>Classe MDM \_ WindowsLicensing

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

A **classe MDM \_ WindowsLicensing** foi projetada para cenários de gerenciamento relacionados ao licenciamento. Atualmente, o escopo é limitado a atualizações de edição de Windows 10 desktop e dispositivos móveis, como Windows 10 Pro para Windows 10 Enterprise. Além disso, esse CSP fornece a capacidade de ativar ou alterar a chave do produto (Product Key) Windows 10 desktop.

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

A **classe MDM \_ WindowsLicensing** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe MDM \_ WindowsLicensing** tem esses métodos.



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
<td style="text-align: left;">Instala uma chave do produto (Product Key) para Windows 10 desktop. Não reinicializa.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>CheckApplicabilityMethod</strong></a></td>
<td style="text-align: left;">Método para verificar se a chave do produto inserida pode ser usada para uma atualização de edição, ativação ou alteração de uma chave do produto Windows 10 para dispositivos da área de trabalho.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>UpgradeEditionWithLicenseMethod</strong></a></td>
<td style="text-align: left;">Forneça uma licença para uma atualização de edição de Windows 10 dispositivos móveis.<br/>
<blockquote>
[!Note]<br />
Esse processo de atualização não requer uma reinicialização do sistema.
</blockquote>
<br/> <br/> O tipo de data é XML.<br/> A operação com suporte é Executar.<br/>
<blockquote>
[!Important]<br />
O conteúdo do arquivo de licença XML deve ser escapado corretamente (ou seja, ele não deve simplesmente ser um XML copiado), caso contrário, a atualização de edição no Windows 10 dispositivos móveis falhará. Para obter mais informações sobre o escape adequado do arquivo de licença XML, consulte a Seção 2.4 da <a href="https://www.w3.org/TR/xml/">especificação XML W3C</a>. O arquivo de licença XML é adquirido do Centro de Serviços de Licenciamento por Volume da Microsoft. Sua organização deve ter um contrato de Licenciamento por Volume com a Microsoft para acessar o portal.
</blockquote>
<br/> A seguir estão os caminhos de atualização de edição válidos ao usar esse nó por meio de um MDM ou pacote de provisionamento:
<ul>
<li>Windows 10 Mobileto Windows 10 Mobile Enterprise<br/></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>UpgradeEditionWithProductKeyMethod</strong></a></td>
<td style="text-align: left;">Dispara o dispositivo para pegar a chave do produto (Product Key) e atualizar a edição do cliente.
<blockquote>
[!Note]<br />
Esse processo de atualização requer uma reinicialização do sistema.
</blockquote>
<br/> <br/> A operação com suporte é Executar.<br/> Quando uma chave do produto (Product Key) é pressionada por um servidor MDM para o dispositivo de um <strong> usuário, </strong> ochangepk.exeé executado usando a chave do produto (Product Key). Após a conclusão, uma notificação é mostrada ao usuário de que uma nova edição do Windows 10 está disponível. Em seguida, o usuário pode reiniciar o sistema manualmente ou, após duas horas, o dispositivo será reiniciado automaticamente para concluir a atualização. O usuário receberá uma notificação de lembrete 10 minutos antes da reinicialização automática.<br/> Depois que o dispositivo for reiniciado, o processo de upgrade de edição será reiniciado. O usuário receberá uma notificação de upgrade bem-sucedido.
<blockquote>
[!Important]<br />
Se outra política exigir uma reinicialização do sistema que ocorre quando <strong>changepk.exe</strong> estiver em execução, a atualização de edição falhará.
</blockquote>
<br/> <br/> Se uma chave do produto (Product Key) for inserida em um pacote de provisionamento e o usuário iniciar a instalação do pacote, uma notificação será mostrada ao usuário dizendo que o sistema será reiniciado para a conclusão da instalação do pacote. Após o consentimento explícito do usuário para continuar, o pacote continua a instalação <strong> e </strong>changepk.exeé executado usando a chave do produto (Product Key). O usuário receberá uma notificação de lembrete 30 segundos antes do reinício automático. <br/> Depois que o dispositivo for reiniciado, o processo de upgrade de edição será reiniciado. O usuário receberá uma notificação de upgrade bem-sucedido. <br/> Esse nó também pode ser usado para ativar ou alterar uma chave do produto (Product Key) em uma edição específica do Windows 10 desktop inserindo uma chave do produto (Product Key). A ativação ou alteração de uma chave do produto (Product Key) não exige uma reinicialização e é um processo silencioso para o usuário.<br/>
<blockquote>
[!Important]<br />
A chave do produto (product key) inserida deve ter 29 caracteres (ou seja, deve incluir traços), caso contrário, a ativação, a atualização de edição ou a alteração da chave do produto (product key) Windows 10 dispositivos da área de trabalho falharão. A chave do produto (Product Key) é adquirida do Centro de Serviços de Licenciamento por Volume da Microsoft. Sua organização deve ter um contrato de Licenciamento por Volume com a Microsoft para acessar o portal.
</blockquote>
<br/> A seguir estão os caminhos de atualização de edição válidos ao usar esse nó por meio de um MDM:
<ul>
<li>Windows 10 Enterprise para Windows 10 Education</li>
<li>Windows 10 Home para Windows 10 Education</li>
<li>Windows 10 Pro para Windows 10 Education</li>
<li>Windows 10 Pro para Windows 10 Enterprise</li>
</ul>
<br/> A ativação ou alteração de uma chave do produto (Product Key) pode ser realizada nas seguintes edições:
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

A **classe MDM \_ WindowsLicensing** tem essas propriedades.

<dl> <dt>

[Edição](/windows/client-management/mdm/windowslicensing-csp#edition)
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
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

[LicenseKeyType](/windows/client-management/mdm/windowslicensing-csp#licensekeytype)
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

</dd> <dt>

**Parentid**
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

Tipo de acesso: Leitura/gravação
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Namespace<br/>                | \\DMMap de \\ MDM cimv2 \\ raiz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Como usar os scripts do PowerShell com o provedor de ponte WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

