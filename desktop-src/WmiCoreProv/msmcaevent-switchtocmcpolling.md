---
description: Representa a manipulação de CMC (verificação de computador) corrigida a ser alternada do driver de interrupção para a sondagem. Essa classe está disponível somente em sistemas de Windows de 64 bits.
ms.assetid: c5e99e13-0f65-40bc-8863-b2ca7ea221df
title: MSMCAEvent_SwitchToCMCPolling classe
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
ms.openlocfilehash: a8192dc83a50063b2aaabba2bf708053fadb8e094bfa1cab82b11b084f722a76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119640936"
---
# <a name="msmcaevent_switchtocmcpolling-class"></a>Classe SwitchToCMCPolling MSMCAEvent \_

A **classe \_ SwitchToCMCPolling MSMCAEvent** representa a manipulação de CMC (verificação de máquina) corrigida a ser alternada do driver de interrupção para a sondagem. Em alguns casos, o kernel sonda a SAL (camada de abstração do sistema) para qualquer CMC ou CPE (erro de plataforma corrigido) que ocorreu dentro do intervalo de sondagem anterior. Essa classe está disponível somente em sistemas de Windows de 64 bits.

A sintaxe a seguir é simplificada Managed Object Format código (MOF) e inclui todas as suas propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MSMCAEvent_SwitchToCMCPolling : WMIEvent
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Membros

A **classe \_ SwitchToCMCPolling MSMCAEvent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ SwitchToCMCPolling MSMCAEvent** tem essas propriedades.

<dl> <dt>

**Ativo**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**TRUE**, se esta instância da classe estiver ativa; caso contrário, **FALSE.**

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **Chave**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Identificador exclusivo dessa instância da classe .

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ SwitchToCMCPolling MSMCAEvent** é derivada de [**WMIEvent.**](wmievent.md)

A SAL (camada de abstração do sistema) é um código gravado na ROM que o sistema operacional chama para executar operações dependentes da plataforma. Ele é semelhante ao BIOS em uma plataforma x86. Nos casos em que a plataforma não dá suporte a interrupções para sondagem de CMC ou CPE, o sistema operacional pesquisa a cada minuto, verificando se ocorreu um erro anteriormente. Se a plataforma dá suporte a interrupções e o sistema operacional recebe uma quantidade definida pelo usuário de pesquisas de CMC ou CPE dentro de um minuto, ela desabilita a interrupção e a sondagem. Se o usuário não definir o número de pesquisas em um minuto, o sistema definirá um padrão para 10 pesquisas por minuto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2003<br/>                                                         |
| Namespace<br/>                | WMI \\ raiz<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MSMCA Classes](msmca-classes.md)
</dt> <dt>

[**Wmievent**](wmievent.md)
</dt> </dl>

 

