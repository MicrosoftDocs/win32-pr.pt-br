---
title: Método IConfigAsfWriter SetIndexMode
description: O método SetIndexMode permite que o aplicativo controle se o arquivo será indexado temporalmente.
ms.assetid: 104e29f4-a1e5-4e26-a9ef-52ef52d6f5b2
keywords:
- Formato de mídia do windows do método SetIndexMode
- Método SetIndexMode windows Formato de mídia, interface IConfigAsfWriter
- IConfigAsfWriter interface windows Media Format , método SetIndexMode
topic_type:
- apiref
api_name:
- IConfigAsfWriter.SetIndexMode
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b65fbd3d279b8a66c132d24476b09b0f897c5993ea9a97d86096cf856832f9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118433605"
---
# <a name="iconfigasfwritersetindexmode-method"></a>Método IConfigAsfWriter::SetIndexMode

O **método SetIndexMode** permite que o aplicativo controle se o arquivo será indexado temporalmente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetIndexMode(
  [in] BOOL bIndexFile
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bIndexFile* \[ Em\]
</dt> <dd>

Variável do **tipo BOOL;** **TRUE** especifica que o arquivo será indexado temporalmente.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará S \_ OK. Se falhar, ele retornará um código **de erro HRESULT.**

## <a name="remarks"></a>Comentários

Por padrão, o [Wm ASF Writer](wm-asf-writer-filter.md) cria arquivos ASF indexados temporalmente. Ele executa a indexação quando o grafo é interrompido. Você poderá desabilitar esse comportamento se quiser fazer sua própria indexação baseada em quadro como uma etapa de pós-processamento. Para criar um arquivo indexado por quadro, chame **SetIndexMode**(FALSE), crie o arquivo e use os métodos do SDK de Formato de Mídia do Windows diretamente para criar um índice baseado em quadro para o arquivo.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**IConfigAsfWriter Interface**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

 