---
description: Adiciona uma parte dos dados específicos do aplicativo.
ms.assetid: 86ba37ac-8e65-4397-8ed1-37463152bebd
title: Método IContextNode::AddPropertyData (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.AddPropertyData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8c9988217aed21ff1142f0e2083bee568ed12c31d90530ac1f3e9f5719c46446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719690"
---
# <a name="icontextnodeaddpropertydata-method"></a>Método IContextNode::AddPropertyData

Adiciona uma parte dos dados específicos do aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AddPropertyData(
  [in] const GUID  *pPropertyDataId,
  [in]       ULONG ulPropertyDataSize,
  [in]       BYTE  *pbPropertiesData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPropertyDataId* \[ Em\]
</dt> <dd>

Um GUID (identificador global exclusivo) usado para identificar o tipo de dados.

</dd> <dt>

*ulPropertyDataSize* \[ Em\]
</dt> <dd>

O tamanho dos dados em bytes.

</dd> <dt>

*pbPropertiesData* \[ Em\]
</dt> <dd>

\[in, size \_ is(ulPropertyDataSize)\]

Uma matriz de inteiros sem sinal de 8 bits que contém as informações de propriedade a adicionar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para ver uma descrição dos valores de retorno, consulte [Classes e interfaces – Análise de Tinta.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Comentários

Use **IContextNode::AddPropertyData para** associar dados a um nó de contexto. Para recuperar os dados posteriormente, use [**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md).

O analisador de tinta pode excluir o nó como parte da análise de tinta, a menos que o nó de contexto seja confirmado (consulte [**IContextNode::Confirm**](icontextnode-confirm.md)). Para obter mais informações sobre como sincronizar os dados do aplicativo com [**o IInkAnalyzer,**](iinkanalyzer.md)consulte [Proxy de dados com análise de tinta.](data-proxy-with-ink-analysis.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| parâmetro<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[**IContextNode::GetPropertyDataIds**](icontextnode-getpropertydataids.md)
</dt> <dt>

[**IContextNode::ContainsPropertyData**](icontextnode-containspropertydata.md)
</dt> <dt>

[**IContextNode::LoadPropertiesData**](icontextnode-loadpropertiesdata.md)
</dt> <dt>

[**IContextNode::RemovePropertyData**](icontextnode-removepropertydata.md)
</dt> <dt>

[**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md)
</dt> </dl>

 

 




