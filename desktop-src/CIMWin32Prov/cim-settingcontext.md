---
description: A \_ classe CIM SettingContext associa objetos de configuração a objetos de configuração.
ms.assetid: 8ed7e150-b4e6-4fd4-809b-32e870b559c4
ms.tgt_platform: multiple
title: Classe CIM_SettingContext
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingContext
- CIM_SettingContext.Context
- CIM_SettingContext.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: df59bff8be90d3db3ac6dfde638120779850f2691bd3e93826c57f829d034a4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919506"
---
# <a name="cim_settingcontext-class"></a>\_Classe CIM SettingContext

A classe **CIM \_ SettingContext** associa objetos de configuração a objetos de configuração. Por exemplo, as configurações de um adaptador de rede podem mudar com base no site ou na rede à qual seu sistema de computador de hospedagem está conectado. Nesse caso, o sistema de computador teria dois objetos de configuração diferentes, correspondentes às diferenças na configuração de rede para os dois segmentos de rede. Uma configuração agregaria um objeto de configuração para o adaptador de rede ao operar em um segmento; enquanto que a outra configuração agregaria um objeto de configuração de adaptador de rede diferente, específico a outro segmento. Observe que muitas configurações de computador são independentes da configuração de rede. Por exemplo, ambas as configurações agregariam o mesmo objeto de configuração para a resolução do monitor do sistema de computador.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{F0B752E8-DB30-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_SettingContext
{
  CIM_Configuration REF Context;
  CIM_Setting       REF Setting;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ SettingContext** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ SettingContext** tem essas propriedades.

<dl> <dt>

**Contexto**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ configuração de CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **agregação**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referência ao objeto de configuração que agrega a configuração.

</dd> <dt>

**Configuração**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ configuração de CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência a uma configuração agregada.

</dd> </dl>

## <a name="remarks"></a>Comentários

O WMI não implementa essa classe.

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

