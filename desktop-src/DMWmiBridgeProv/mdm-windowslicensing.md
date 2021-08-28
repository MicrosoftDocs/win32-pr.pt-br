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
ms.openlocfilehash: ca9470b72cb6a50323af9294be4a6506682fc7aa
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480922"
---
# <a name="mdm_windowslicensing-class"></a>\_Classe WindowsLicensing do MDM

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

A classe **MDM \_ WindowsLicensing** foi projetada para cenários de gerenciamento relacionados ao licenciamento. atualmente, o escopo é limitado a atualizações de edição do Windows 10 área de trabalho e dispositivos móveis, como Windows 10 Pro para Windows 10 Enterprise. além disso, esse CSP fornece a capacidade de ativar ou alterar a chave do produto de dispositivos Windows 10 desktop.

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




| Método | Descrição | 
|--------|-------------|
| <a href="mdm-windowslicensing-changeproductkeymethod.md"><strong>ChangeProductKeyMethod</strong></a> | instala uma chave do produto para dispositivos Windows 10 desktop. Não reinicia.<br /> | 
| <a href="mdm-windowslicensing-checkapplicabilitymethod.md"><strong>CheckApplicabilityMethod</strong></a> | método para verificar se a chave do produto (product key) inserida pode ser usada para uma atualização de edição, ativar ou alterar uma chave do produto de Windows 10 para dispositivos desktop.<br /> | 
| <a href="mdm-windowslicensing-upgradeeditionwithlicensemethod.md"><strong>UpgradeEditionWithLicenseMethod</strong></a> | forneça uma licença para uma atualização de edição de dispositivos móveis Windows 10.<br /><blockquote>[!Note]<br />Esse processo de atualização não exige uma reinicialização do sistema.</blockquote><br /><br /> O tipo de data é XML.<br /> A operação com suporte é executada.<br /><blockquote>[!Important]<br />o conteúdo do arquivo de licença XML deve ter um escape adequado (ou seja, não deve simplesmente ser um XML copiado), caso contrário, a atualização de edição em dispositivos Windows 10 móveis falhará. Para obter mais informações sobre a saída correta do arquivo de licença XML, consulte a seção 2,4 da <a href="https://www.w3.org/TR/xml/">especificação XML do W3C</a>. O arquivo de licença XML é adquirido do centro de serviços de licenciamento por volume da Microsoft. Sua organização deve ter um contrato de licenciamento por volume com a Microsoft para acessar o Portal.</blockquote><br /> Estes são os caminhos de atualização de edição válidos ao usar este nó por meio de um pacote MDM ou de provisionamento:<ul><li>Windows 10 Windows 10 Mobile Enterprise móvel<br /></li></ul><br /> | 
| <a href="mdm-windowslicensing-upgradeeditionwithproductkeymethod.md"><strong>UpgradeEditionWithProductKeyMethod</strong></a> | Dispara o dispositivo para pegar a chave do produto e atualizar a edição do cliente.<blockquote>[!Note]<br />Esse processo de atualização requer uma reinicialização do sistema.</blockquote><br /><br /> A operação com suporte é executada.<br /> Quando uma chave do produto é enviada por push de um servidor MDM para um dispositivo do usuário, o <strong>changepk.exe</strong> é executado usando a chave do produto. após a conclusão, uma notificação é mostrada ao usuário de que uma nova edição do Windows 10 está disponível. O usuário pode reiniciar o sistema manualmente ou, após duas horas, o dispositivo será reiniciado automaticamente para concluir a atualização. O usuário receberá uma notificação de lembrete 10 minutos antes da reinicialização automática.<br /> Depois que o dispositivo for reiniciado, o processo de upgrade de edição será reiniciado. O usuário receberá uma notificação de upgrade bem-sucedido.<blockquote>[!Important]<br />Se outra política exigir uma reinicialização do sistema que ocorra quando <strong>changepk.exe</strong> estiver em execução, a atualização da edição falhará.</blockquote><br /><br /> Se uma chave do produto (Product Key) for inserida em um pacote de provisionamento e o usuário iniciar a instalação do pacote, uma notificação será mostrada ao usuário dizendo que o sistema será reiniciado para a conclusão da instalação do pacote. Após o consentimento explícito do usuário para continuar, o pacote continua a instalação e <strong>changepk.exe</strong> é executado usando a chave do produto. O usuário receberá uma notificação de lembrete 30 segundos antes do reinício automático. <br /> Depois que o dispositivo for reiniciado, o processo de upgrade de edição será reiniciado. O usuário receberá uma notificação de upgrade bem-sucedido. <br /> esse nó também pode ser usado para ativar ou alterar uma chave do produto (product key) em uma edição específica do dispositivo Windows 10 desktop inserindo uma chave do produto (product key). A ativação ou a alteração de uma chave do produto não requer uma reinicialização e é um processo silencioso para o usuário.<br /><blockquote>[!Important]<br />a chave do produto (product key) inserida deve ter 29 caracteres (ou seja, deve incluir traços), caso contrário, a ativação, a atualização de edição ou a alteração da chave do produto em Windows 10 dispositivos de área de trabalho falharão. A chave do produto é adquirida do centro de serviços de licenciamento por volume da Microsoft. Sua organização deve ter um contrato de licenciamento por volume com a Microsoft para acessar o Portal.</blockquote><br /> Estes são os caminhos de atualização de edição válidos ao usar este nó por meio de um MDM:<ul><li>Windows 10 Enterprise Windows 10 Education</li><li>Windows 10 Home Windows 10 Education</li><li>Windows 10 Pro Windows 10 Education</li><li>Windows 10 Pro Windows 10 Enterprise</li></ul><br /> A ativação ou a alteração de uma chave do produto pode ser executada nas seguintes edições:<ul><li>Windows 10 Education</li><li>Windows 10 Enterprise</li><li>Windows 10 Home</li><li>Windows 10 Pro</li></ul><br /> | 




 

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
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                      |
| Namespace<br/>                | \\DMMap de \\ MDM \\ CIMv2 raiz<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Como usar os scripts do PowerShell com o provedor de ponte WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

