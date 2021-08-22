---
description: Essa classe é a classe de tipo de evento para eventos de rede. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: afa994ef-dd1c-4909-a6cd-7021be4fff40
title: SystemConfig_Network classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Network
- SystemConfig_Network.TcbTablePartitions
- SystemConfig_Network.MaxHashTableSize
- SystemConfig_Network.MaxUserPort
- SystemConfig_Network.TcpTimedWaitDelay
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6b196e8c1ad5a997642cc48491e9d1a4b5e73bc26db71d5ea5258f7cf162a00a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069686"
---
# <a name="systemconfig_network-class"></a>Classe SystemConfig \_ Network

Essa classe é a classe de tipo de evento para eventos de rede.

A sintaxe a seguir é simplificada do código MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[EventType(17), EventTypeName("Network")]
class SystemConfig_Network : SystemConfig
{
  uint32 TcbTablePartitions;
  uint32 MaxHashTableSize;
  uint32 MaxUserPort;
  uint32 TcpTimedWaitDelay;
};
```

## <a name="members"></a>Membros

A **classe SystemConfig \_ Network** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe SystemConfig \_ Network** tem essas propriedades.

<dl> <dt>

**MaxHashTableSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(2)
</dt> </dl>

O tamanho da tabela de hash na qual os blocos de controle TCP (TCBs) são armazenados. O TCP armazena blocos de controle em uma tabela de hash para que possa encontrá-los muito rapidamente.

</dd> <dt>

**Maxuserport**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(3)
</dt> </dl>

O número de porta mais alto que o TCP pode atribuir quando um aplicativo solicita uma porta de usuário disponível do sistema. Normalmente, as portas efêmeras (aquelas usadas brevemente) são alocadas aos números de porta 1024 a 5000.

O valor para o número de porta de usuário mais alto que o TCP pode atribuir é controlado por uma configuração do Registro. Para obter mais informações, [consulte MaxUserPort.](/previous-versions/windows/it-pro/windows-2000-server/cc938196(v=technet.10))

</dd> <dt>

**TcbTablePartitions**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(1)
</dt> </dl>

O número de partições na tabela Bloco de Controle de Transporte. O particionamento da tabela Bloco de Controle de Transporte minimiza a contenção para acesso à tabela. Isso é especialmente útil em sistemas multiprocessadores.

</dd> <dt>

**Tcptimedwaitdelay**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: WmiDataId(4)
</dt> </dl>

O tempo que deve passar antes que o TCP possa liberar uma conexão fechada e reutilizar seus recursos. Esse intervalo entre o fechamento e a versão é conhecido como o estado TIME \_ WAIT ou o estado 2MSL. Durante esse tempo, a conexão pode ser reabrida com muito menos custo para o cliente e o servidor do que estabelecer uma nova conexão.

O RFC 793 publicado pelo IETF requer que o TCP mantenha uma conexão fechada por um intervalo pelo menos igual a duas vezes o tempo de vida máximo do segmento (2MSL) da rede. Quando uma conexão é liberada, seu par de soquetes e o bloco de controle TCP (TCB) podem ser usados para dar suporte a outra conexão. Por padrão, a MSL é definida como 120 segundos e o valor dessa entrada é igual a duas MSLs ou 4 minutos. Para obter mais informações, [consulte RFC 793](https://tools.ietf.org/html/rfc973).

Reduzir o valor dessa entrada usando uma configuração do Registro permite que o TCP libere conexões fechadas mais rapidamente, fornecendo mais recursos para novas conexões. No entanto, se o valor for muito baixo, o TCP poderá liberar recursos de conexão antes da conexão ser concluída, exigindo que o servidor use recursos adicionais para restabelecer a conexão.

Normalmente, o TCP não libera conexões fechadas até que o valor dessa entrada expire. No entanto, o TCP pode liberar conexões antes que esse valor expire se estiver ficando sem TCBs (blocos de controle TCP). O número de TCBs que o sistema cria é controlado por uma configuração do Registro. Para obter mais informações, [consulte MaxFreeTCBs](/previous-versions/windows/it-pro/windows-2000-server/cc938178(v=technet.10)).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 
