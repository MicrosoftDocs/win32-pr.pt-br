---
description: Uma classe base abstrata da qual todas as classes de dados do provedor de arquitetura de verificação de máquina (MCA), como MSMCAInfo \_ RawMCAData, são derivadas. essa classe está disponível somente em sistemas Windows de 64 bits.
ms.assetid: 22ec8343-fc4f-4b14-9354-26b5d6a6fe09
title: Classe MSMCAInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: cef9878ea8e9dd6c11c6b18a62d332e17f24810548360e0edb9c117e02a710c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051184"
---
# <a name="msmcainfo-class"></a>Classe MSMCAInfo

A classe **MSMCAInfo** é uma classe base abstrata da qual todas as classes de dados do provedor de arquitetura de verificação de máquina (MCA), como [**MSMCAInfo \_ RawMCAData**](msmcainfo-rawmcadata.md), são derivadas. O provedor MCA também tem classes de evento, derivadas de [**WmiEvent**](wmievent.md). essa classe está disponível somente em sistemas Windows de 64 bits.

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class MSMCAInfo
{
};
```

## <a name="members"></a>Membros

A classe **MSMCAInfo** não define nenhum membro.

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

[**\_Cabeçalho MSMCAEvent**](msmcaevent-header.md)
</dt> <dt>

[**WMIEvent**](wmievent.md)
</dt> </dl>

 

 




