---
description: Recupera uma matriz que contém os dados de Propriedade do pacote para o traço especificado.
ms.assetid: 02db48b3-edc3-4ecb-8103-79312194937a
title: 'Método IContextNode:: GetStrokePacketDataById (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.GetStrokePacketDataById
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: be2e9326e2ecb20afc652776c006c8ae989c7396
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105794620"
---
# <a name="icontextnodegetstrokepacketdatabyid-method"></a>Método IContextNode:: GetStrokePacketDataById

Recupera uma matriz que contém os dados de Propriedade do pacote para o traço especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetStrokePacketDataById(
  [in]      LONG  strokeId,
  [in, out] ULONG *pStrokePacketDataCount,
  [out]     LONG  **pplStrokePacketData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strokeid* \[ no\]
</dt> <dd>

O identificador para o traço.

</dd> <dt>

*pStrokePacketDataCount* \[ entrada, saída\]
</dt> <dd>

O comprimento da matriz de dados do pacote.

</dd> <dt>

*pplStrokePacketData* \[ fora\]
</dt> <dd>

Um ponteiro para os dados do pacote para o traço.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para obter uma descrição dos valores de retorno, consulte [classes e interfaces – análise de tinta](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Comentários

> [!Caution]  
> Para evitar um vazamento de memória, use [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) para liberar a memória do \* *pplStrokePacketData* quando você não precisar mais das informações.

 

*plStrokePacketData* contém dados de pacote para todos os pontos no traço. Para obter os tipos de dados de pacote incluídos para cada ponto no traço, use [**IContextNode:: GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md).

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

[**IContextNode::GetStrokePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

