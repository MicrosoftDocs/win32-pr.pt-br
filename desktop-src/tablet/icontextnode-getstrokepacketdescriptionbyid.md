---
description: Recupera uma matriz que contém os identificadores de propriedade de pacote para o traço especificado.
ms.assetid: 169e3ce3-fb81-4ed6-b380-ef0d12444ba7
title: 'Método IContextNode:: GetStrokePacketDescriptionById (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDescriptionById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e1633cd2097e256d389a2c86e450bf221f0546f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760987"
---
# <a name="icontextnodegetstrokepacketdescriptionbyid-method"></a>Método IContextNode:: GetStrokePacketDescriptionById

Recupera uma matriz que contém os identificadores de propriedade de pacote para o traço especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStrokePacketDescriptionById(
  [in]      LONG  lStrokeId,
  [in, out] ULONG *pulStrokePacketDescriptionCount,
  [out]     GUID  **ppStrokePacketDescriptionGuids
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lStrokeId* \[ no\]
</dt> <dd>

O identificador para o traço.

</dd> <dt>

*pulStrokePacketDescriptionCount* \[ entrada, saída\]
</dt> <dd>

O número de propriedades do pacote em cada pacote.

</dd> <dt>

*ppStrokePacketDescriptionGuids* \[ fora\]
</dt> <dd>

Uma matriz que contém os identificadores de Propriedade do pacote.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória do \* *ppStrokePacketDescriptionGuids* quando você não precisar mais das informações.

 

\**ppStrokePacketDescriptionGuids* contém os identificadores globalmente exclusivos (GUIDs) que descrevem os tipos de dados de pacote incluídos para cada ponto no traço. Para obter uma lista completa das propriedades de pacote disponíveis, consulte [constantes PacketPropertyGuids](packetpropertyguids-constants.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom. h (também requer IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::GetStrokePacketDataById**](icontextnode-getstrokepacketdatabyid.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

