---
description: Representa os parâmetros para copiar um arquivo do host para o convidado.
ms.assetid: 255F4132-C212-4A3B-A9B8-3F531E7D1CF9
title: Classe Msvm_CopyFileToGuestSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestSettingData
- Msvm_CopyFileToGuestSettingData.Description
- Msvm_CopyFileToGuestSettingData.Caption
- Msvm_CopyFileToGuestSettingData.InstanceID
- Msvm_CopyFileToGuestSettingData.ElementName
- Msvm_CopyFileToGuestSettingData.OverwriteExisting
- Msvm_CopyFileToGuestSettingData.CreateFullPath
- Msvm_CopyFileToGuestSettingData.SourcePath
- Msvm_CopyFileToGuestSettingData.DestinationPath
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6eb011ec8d03153bd5f1b7d956775327d2582410e9ca12591e19a39ddb4af5fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148835"
---
# <a name="msvm_copyfiletoguestsettingdata-class"></a>\_Classe Msvm CopyFileToGuestSettingData

Representa os parâmetros para copiar um arquivo do host para o convidado. Essa classe deriva do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[AMENDMENT]
class Msvm_CopyFileToGuestSettingData : CIM_SettingData
{
  string  Description;
  string  Caption;
  string  InstanceID;
  string  ElementName;
  boolean OverwriteExisting;
  boolean CreateFullPath;
  string  SourcePath;
  string  DestinationPath;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ CopyFileToGuestSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ CopyFileToGuestSettingData** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **maxlen** (64)
</dt> </dl>

Uma breve descrição textual do objeto.

</dd> <dt>

**Createfullpath**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se os diretórios ausentes no caminho do arquivo de destino devem ser criados antes de copiar o arquivo.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição textual do objeto.

</dd> <dt>

**DestinationPath**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho completo do arquivo de destino a ser copiado. Esse arquivo de destino deve ser acessível para o convidado e pode conter variáveis de ambiente, que são expandidas pelo convidado. Se o caminho especificado for um diretório existente no convidado, o arquivo de destino será criado nesse diretório. Nesse caso, o nome do arquivo de **SourcePath** é usado como o nome do arquivo de destino.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome de exibição para esta instância de SettingData. Além disso, o nome de exibição pode ser usado como uma propriedade de índice para uma pesquisa ou consulta. (Observação: o nome não precisa ser exclusivo em um namespace.)

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Dentro do escopo do namespace de instanciação, a InstanceID identifica de forma opaca e exclusiva uma instância dessa classe. Para garantir a exclusividade no NameSpace, o valor de InstanceID deve ser construído usando o seguinte algoritmo "preferencial": *OrgID*:*LocalId* em que *OrgID* e *LocalId* são separados por dois-pontos (:) e onde *OrgID* deve incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios que está criando ou definindo a InstanceId ou que é uma ID registrada atribuída à entidade de negócios por uma autoridade global reconhecida. (Esse requisito é semelhante ao *SchemaName* \_ Estrutura *ClassName* de nomes de classe de esquema.) Além disso, para garantir a exclusividade, *OrgID* não deve conter dois-pontos (:). Ao usar esse algoritmo, os primeiros dois-pontos para aparecer em InstanceID devem aparecer entre *OrgID* e *LocalId*. A *LocalId* é escolhida pela entidade de negócios e não deve ser reutilizada para identificar elementos subjacentes (reais) diferentes. Se o algoritmo preferencial acima não for usado, a entidade de definição deverá garantir que a InstanceID resultante não seja reutilizada em quaisquer InstanceIDs produzidas por esse ou outros provedores para o NameSpace dessa instância. Para instâncias definidas por DMTF, o algoritmo "preferencial" deve ser usado com o *OrgID* definido como CIM.

</dd> <dt>

**OverwriteExisting**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se um arquivo de destino existente deve ser substituído.

</dd> <dt>

**SourcePath**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O caminho completo do arquivo de origem a ser copiado. Esse arquivo de origem deve ser acessível para o host Hyper-V e pode conter variáveis de ambiente, que são expandidas pelo host Hyper-V.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ somente aplicativos da área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                                                 |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))
</dt> </dl>

 

