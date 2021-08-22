---
description: Executa um script predefinido em uma linguagem de script arbitrária quando um evento é entregue a ele.
ms.assetid: 2c0aa216-4255-49ff-9bbd-d6c62b5b9139
ms.tgt_platform: multiple
title: Classe ActiveScriptEventConsumer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActiveScriptEventConsumer
- ActiveScriptEventConsumer.CreatorSID
- ActiveScriptEventConsumer.KillTimeout
- ActiveScriptEventConsumer.MachineName
- ActiveScriptEventConsumer.MaximumQueueSize
- ActiveScriptEventConsumer.Name
- ActiveScriptEventConsumer.ScriptingEngine
- ActiveScriptEventConsumer.ScriptFileName
- ActiveScriptEventConsumer.ScriptText
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: acf7ef4b4207f72cbaee61c0aaad8b2279419682bdddbeb4373c36c6868b8fce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118557829"
---
# <a name="activescripteventconsumer-class"></a>Classe ActiveScriptEventConsumer

A classe **ActiveScriptEventConsumer** executa um script predefinido em uma linguagem de script arbitrária quando um evento é entregue a ele. Essa classe é um dos consumidores de eventos padrão que o WMI fornece. Para obter mais informações, consulte [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md).


```cmd
Mofcomp -n:root\<namespace> scrcons.mof
```



Você pode configurar o desempenho de todas as instâncias do **ActiveScriptEventConsumer** em um sistema definindo os valores da propriedade [**Timeout**](scriptingstandardconsumersetting.md) ou **MaximumScripts** na instância única de **ScriptingStandardConsumerSetting**.

## <a name="syntax"></a>Sintaxe

``` syntax
[AMENDMENT]
class ActiveScriptEventConsumer : __EventConsumer
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  uint32 KillTimeout = 0;
  string MachineName;
  uint32 MaximumQueueSize;
  string Name;
  string ScriptingEngine;
  string ScriptFileName;
  string ScriptText;
};
```

## <a name="members"></a>Membros

A classe **ActiveScriptEventConsumer** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **ActiveScriptEventConsumer** tem essas propriedades.

<dl> <dt>

**CreatorSID**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Matriz que representa o identificador de segurança (SID), que identifica exclusivamente o criador do consumidor de evento de script ativo. Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**KillTimeout**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número, em segundos, que o script tem permissão para ser executado. Se 0 (zero), que é o padrão, o script não será encerrado.

</dd> <dt>

**MachineName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome do computador para o qual o WMI envia eventos. Por convenção de consumidores padrão da Microsoft, o consumidor de scripts não pode ser executado remotamente. Os consumidores de terceiros também podem usar essa propriedade. Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**MaximumQueueSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Máximo de fila, em bytes, para o consumidor de evento de script ativo. Essa propriedade é herdada de [**\_ \_ EventConsumer**](--eventconsumer.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [ **chave**](standard-qualifiers.md)
</dt> </dl>

Identificador exclusivo para o consumidor do evento. Se você renomear o consumidor, o resultado será dois consumidores iguais que têm nomes diferentes.

</dd> <dt>

**ScriptFileName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome do arquivo do qual o texto do script é lido, pretendido como uma alternativa para especificar o texto do script na propriedade **ScriptText** . Essa propriedade deverá ser **nula** se a propriedade **ScriptText** não for **nula**.

> [!Note]  
> Quando você especifica o **ScriptFileName**, é importante proteger o executável que você está iniciando. Se o executável não estiver em um local seguro ou protegido com uma ACL (lista de controle de acesso) forte, qualquer pessoa poderá substituir o executável por um diferente. Para obter mais informações sobre ACLs, consulte [criando um descritor de segurança (SD) para um novo objeto em C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

 

</dd> <dt>

**ScriptingEngine**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome do mecanismo de script a ser usado, por exemplo, "VBScript". Esta propriedade não pode ser **nula**.

</dd> <dt>

**ScriptText**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Texto do script expresso em uma linguagem conhecida pelo mecanismo de script. Essa propriedade deverá ser **nula** se a propriedade **ScriptFileName** não for **nula**.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa classe é derivada da classe abstrata [**\_ \_ EventConsumer**](--eventconsumer.md) . Ele está localizado no namespace da \\ assinatura raiz.

Quando o texto de um script é especificado na instância do consumidor de eventos, o script tem acesso à instância de evento na variável de ambiente de script **TargetEvent**.

Os scripts são executados no contexto de segurança LocalSystem. Como medida de segurança, somente um administrador do sistema local ou um administrador de domínio pode configurar o consumidor de scripts. Os direitos de acesso não são verificados até o tempo de execução. Depois que o consumidor é configurado, qualquer usuário pode disparar o evento que faz o script.

A falha ao carregar o mecanismo de script ou a análise e validação do script é considerada uma falha. Os códigos de retorno de erro do script e o encerramento do script usando um tempo limite também são considerados falhas.

O **ScriptText** ou o **ScriptFileName** não deve ser **nulo**. Se ambas as propriedades forem **nulas** ou não **nulas**, um erro será gerado.

Quando o WMI é executado como um serviço, os scripts executados por **ActiveScriptEventConsumer** não geram a saída da tela. Scripts que usam **MsgBox** são executados, mas não exibem informações na tela. Não há suporte para a execução do serviço WMI como um arquivo executável, mas o WMI permite que os scripts que usam a função **MsgBox** exibam a saída ou aceitem a entrada do usuário. nenhum dos métodos fornecidos pelo objeto [WScript](/previous-versions//at5ydy31(v=vs.85)) pode ser usado porque **ActiveScriptEventConsumer** não usa Windows Host de Script (WSH).

## <a name="examples"></a>Exemplos

O exemplo de [criar registro de evento WMI permanente para monitorar arquivos](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) no PowerShell na galeria do TechNet usa **ActiveScriptEventConsumer** como parte de um script complexo para configurar um registro de evento do WMI permanente.

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

[Classes de consumidor padrão](standard-consumer-classes.md)
</dt> <dt>

[Executando um script com base em um evento](running-a-script-based-on-an-event.md)
</dt> <dt>

[Recebendo eventos em todos os momentos](receiving-events-at-all-times.md)
</dt> <dt>

[Criando um consumidor lógico](creating-a-logical-consumer.md)
</dt> <dt>

[**\_\_EventConsumer**](--eventconsumer.md)
</dt> <dt>

[**ScriptingStandardConsumerSetting**](scriptingstandardconsumersetting.md)
</dt> </dl>

 

