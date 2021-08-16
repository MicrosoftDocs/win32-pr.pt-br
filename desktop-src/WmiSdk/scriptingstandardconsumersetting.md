---
description: A classe singleton ScriptingStandardConsumerSetting fornece dados de registro que são comuns a todas as instâncias da classe consumidor padrão ActiveScriptEventConsumer.
ms.assetid: d217e058-3529-4173-b896-ebff3d7b05c6
ms.tgt_platform: multiple
title: Classe ScriptingStandardConsumerSetting
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScriptingStandardConsumerSetting
- ScriptingStandardConsumerSetting.Caption
- ScriptingStandardConsumerSetting.Description
- ScriptingStandardConsumerSetting.MaximumScripts
- ScriptingStandardConsumerSetting.SettingID
- ScriptingStandardConsumerSetting.Timeout
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: a69d30511d01fba2df39483d1f76616bfae7c92812ce75989fd0c23558558b33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316200"
---
# <a name="scriptingstandardconsumersetting-class"></a>Classe ScriptingStandardConsumerSetting

A classe singleton **ScriptingStandardConsumerSetting** fornece dados de registro que são comuns a todas as instâncias da classe consumidor padrão [**ActiveScriptEventConsumer**](activescripteventconsumer.md) . Uma instância de **ActiveScriptEventConsumer** usa as propriedades **MaximumScripts** e **Timeout** . Para obter mais informações, consulte [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Singleton, AMENDMENT]
class ScriptingStandardConsumerSetting : CIM_Setting
{
  string Caption = "Scripting Standard Consumer Setting";
  string Description = "Registration data common to all instances of the Scripting Standard Consumer";
  uint32 MaximumScripts = 300;
  string SettingID = "ScriptingStandardConsumerSetting";
  uint32 Timeout = 0;
};
```

## <a name="members"></a>Membros

A classe **ScriptingStandardConsumerSetting** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **ScriptingStandardConsumerSetting** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](standard-qualifiers.md) (64)
</dt> </dl>

Uma breve descrição de um objeto de uma cadeia de caracteres de uma linha. Contém a cadeia de caracteres **ScriptingStandardConsumerSetting** porque esta é uma classe singleton.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição de texto de um objeto.

</dd> <dt>

**MaximumScripts**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Número máximo de scripts que são executados antes que um consumidor inicie uma nova instância. Para limpar os vazamentos de memória de scripts, desligue o consumidor regularmente. O valor padrão é 300.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](standard-qualifiers.md) (256)
</dt> </dl>

Identificador para o objeto de configuração.

</dd> <dt>

**Tempo Limite**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**unidades**](standard-qualifiers.md) ("minutos")
</dt> </dl>

Número máximo de minutos antes que um consumidor inicie uma nova instância. Se for 0 (zero), a propriedade **MaximumScripts** controlará o tempo de vida do consumidor. O intervalo válido para **Timeout** é de 0 a 71.000 e o valor padrão é 0 (zero).

</dd> </dl>

## <a name="remarks"></a>Comentários

A única instância da classe **ScriptingStandardConsumerSetting** reside no \\ namespace raiz cimv2.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Namespace<br/>                | \\Assinatura raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Scrcons. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scrcons.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configuração de CIM \_**](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> <dt>

[Classes de consumidor padrão](standard-consumer-classes.md)
</dt> <dt>

[Executando um script com base em um evento](running-a-script-based-on-an-event.md)
</dt> <dt>

[Criando um consumidor lógico](creating-a-logical-consumer.md)
</dt> <dt>

[Recebendo eventos em todos os momentos](receiving-events-at-all-times.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> </dl>

 

