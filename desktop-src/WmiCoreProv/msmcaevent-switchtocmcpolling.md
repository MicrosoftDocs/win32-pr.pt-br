---
description: Representa a manipulação de verificação de máquina (CMC) corrigida a ser alternada do driver de interrupção para sondagem. Essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: c5e99e13-0f65-40bc-8863-b2ca7ea221df
title: Classe MSMCAEvent_SwitchToCMCPolling
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SwitchToCMCPolling
- MSMCAEvent_SwitchToCMCPolling.Active
- MSMCAEvent_SwitchToCMCPolling.InstanceName
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: f7d0d543dc36054550d4ddf6cc1a77ce80cf1647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296338"
---
# <a name="msmcaevent_switchtocmcpolling-class"></a>\_Classe MSMCAEvent SwitchToCMCPolling

A classe **MSMCAEvent \_ SwitchToCMCPolling** representa a manipulação de verificação de máquina corrigida (CMC) a ser alternada do driver de interrupção para sondagem. Em alguns casos, o kernel sonda a camada de abstração do sistema (SAL) para qualquer erro de plataforma CMC ou correção (CPE) que ocorreu dentro do intervalo de sondagem anterior. Essa classe está disponível somente em sistemas Windows de 64 bits.

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MSMCAEvent_SwitchToCMCPolling : WMIEvent
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Membros

A classe **MSMCAEvent \_ SwitchToCMCPolling** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **MSMCAEvent \_ SwitchToCMCPolling** tem essas propriedades.

<dl> <dt>

**Ativo**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**True**, se esta instância da classe estiver ativa; caso contrário, **false**.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Identificador exclusivo desta instância da classe.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **MSMCAEvent \_ SwitchToCMCPolling** é derivada de [**WmiEvent**](wmievent.md).

A camada de abstração do sistema (SAL) é o código gravado na ROM que o sistema operacional chama para executar operações dependentes da plataforma. É semelhante ao BIOS em uma plataforma x86. Nos casos em que a plataforma não dá suporte a interrupções para sondagem de CMC ou CPE, o sistema operacional é sondado a cada minuto, verificando se ocorreu um erro anteriormente. Se a plataforma der suporte a interrupções e o sistema operacional receber uma quantidade definida pelo usuário de pesquisas CMC ou CPE dentro de um minuto, ele desabilitará a interrupção e a sondagem. Se o usuário não definir o número de pesquisas em um minuto, o sistema definirá um padrão para 10 pesquisas por minuto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2003<br/>                                                         |
| Namespace<br/>                | \\WMI raiz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Classes MSMCA](msmca-classes.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

