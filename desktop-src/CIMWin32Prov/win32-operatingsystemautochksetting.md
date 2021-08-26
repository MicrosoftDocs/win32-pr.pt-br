---
description: Essa classe representa a associação entre um sistema operacional e as configurações de autochk que se aplicam aos discos no computador. Observe que a configuração está associada ao sistema operacional em vez do sistema de computador, pois pode haver um ou mais sistemas operacionais instalados no computador, cada um com suas próprias configurações de autochk.
ms.assetid: 11178459-85c2-41c0-83b3-5b967e3311cf
ms.tgt_platform: multiple
title: Win32_OperatingSystemAutochkSetting classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cfa6e90828935dda8aa163967985813526042b8800f91cb01825fbd158f8a63d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972536"
---
# <a name="win32_operatingsystemautochksetting-class"></a>Classe Win32 \_ OperatingSystemAutochkSetting

Essa classe representa a associação entre um sistema operacional e as configurações de autochk que se aplicam aos discos no computador. Observe que a configuração está associada ao sistema operacional em vez do sistema de computador, pois pode haver um ou mais sistemas operacionais instalados no computador, cada um com suas próprias configurações de autochk.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32a"), AMENDMENT]
class Win32_OperatingSystemAutochkSetting : CIM_ElementSetting
{
  Win32_OperatingSystem REF Element;
  Win32_AutochkSetting  REF Setting;
};
```

## <a name="members"></a>Membros

A **classe \_ OperatingSystemAutochkSetting do Win32** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ OperatingSystemAutochkSetting do Win32** tem essas propriedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de dados: **Sistema Operacional \_ Win32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](../wmisdk/standard-qualifiers.md) ("Elemento"), [**chave**](../wmisdk/key-qualifier.md)
</dt> </dl>

TBD

</dd> <dt>

**Configuração**
</dt> <dd> <dl> <dt>

Tipo de dados: **Win32 \_ AutochkSetting**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](../wmisdk/standard-qualifiers.md) ("Configuração"), [**chave**](../wmisdk/key-qualifier.md)
</dt> </dl>

TBD

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CimWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento \_ CIMSetting**](cim-elementsetting.md)
</dt> </dl>

 

 
