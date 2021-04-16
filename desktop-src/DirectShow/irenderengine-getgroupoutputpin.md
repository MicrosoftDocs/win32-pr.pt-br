---
description: O método GetGroupOutputPin recupera o pino de saída para o grupo especificado.
ms.assetid: be4e17b6-15bf-43b1-8d93-d52d08c8bce6
title: 'Método IRenderEngine:: GetGroupOutputPin (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetGroupOutputPin
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 21e603e15f598c6d493e179a147391cb941a6c7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757673"
---
# <a name="irenderenginegetgroupoutputpin-method"></a>Método IRenderEngine:: GetGroupOutputPin

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `GetGroupOutputPin` método recupera o pino de saída para o grupo especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetGroupOutputPin(
        long Group,
  [out] IPin **ppRenderPin
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Grupo* 
</dt> <dd>

Índice de base zero que especifica o grupo.

</dd> <dt>

*ppRenderPin* \[ fora\]
</dt> <dd>

Recebe um ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de saída.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor **HRESULT** . Os possíveis valores incluem os seguintes:



| Código de retorno                                                                                                  | Descrição                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**\_falso**</dt> </dl>                      | O grupo não tem um pino de saída.<br/>                              |
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Êxito.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | Argumento inválido.<br/>                                               |
| <dl> <dt>**E \_ deve \_ iniciar o \_ renderizador**</dt> </dl>       | Falha ao inicializar o mecanismo de renderização.<br/>                             |
| <dl> <dt>**\_ponteiro E**</dt> </dl>                    | Ponteiro inválido.<br/>                                                |
| <dl> <dt>**o \_ mecanismo de renderização E \_ \_ está \_ desfeito**</dt> </dl> | Falha na operação porque o projeto não foi renderizado com êxito.<br/> |
| <dl> <dt>**E \_ inesperado**</dt> </dl>                 | Erro inesperado.<br/>                                               |



 

## <a name="remarks"></a>Comentários

Antes de chamar esse método, chame [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) para criar o front-end do grafo. Cada grupo representa um único fluxo de mídia e o front-end tem um pino de saída correspondente.

Você pode usar esse método para criar a parte de renderização de um grafo de gravação de arquivos. Conecte os Pins de saída aos filtros do Multiplexador e aos filtros do gravador de arquivo. Para obter mais informações, consulte [renderizando um projeto](rendering-a-project.md).

Para visualização, você não precisa chamar esse método. Basta chamar **ConnectFrontEnd** seguido de [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md).

Se o método retornar S \_ OK, a interface **IPin** que ele retornar terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IRenderEngine**](irenderengine.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




