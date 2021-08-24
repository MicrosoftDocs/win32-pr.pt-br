---
description: O método GetGroupOutputPin recupera o pino de saída para o grupo especificado.
ms.assetid: be4e17b6-15bf-43b1-8d93-d52d08c8bce6
title: Método IRenderEngine::GetGroupOutputPin (Qedit.h)
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
ms.openlocfilehash: 99a1f3c60dcafdda219dc8a05f5523d7c2386249ff500bbb9abb463294ca7239
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767146"
---
# <a name="irenderenginegetgroupoutputpin-method"></a>Método IRenderEngine::GetGroupOutputPin

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

Índice baseado em zero que especifica o grupo.

</dd> <dt>

*ppRenderPin* \[ out\]
</dt> <dd>

Recebe um ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de saída.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **valor HRESULT.** Os possíveis valores incluem os seguintes:



| Código de retorno                                                                                                  | Descrição                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                      | O grupo não tem um pino de saída.<br/>                              |
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Êxito.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | Argumento inválido.<br/>                                               |
| <dl> <dt>**E \_ DEVE \_ INIT \_ RENDERER**</dt> </dl>       | Falha na inicialização do mecanismo de renderização.<br/>                             |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>                    | Ponteiro inválido.<br/>                                                |
| <dl> <dt>**O \_ MECANISMO \_ DE RENDERIZAÇÃO E ESTÁ \_ \_ DESFEITO**</dt> </dl> | Falha na operação porque o projeto não foi renderizado com êxito.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>                 | Erro inesperado.<br/>                                               |



 

## <a name="remarks"></a>Comentários

Antes de chamar esse método, chame [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) para criar o front-end do grafo. Cada grupo representa um único fluxo de mídia e o front-end tem um pino de saída correspondente.

Você pode usar esse método para criar a parte de renderização de um grafo de escrita de arquivo. Conexão os pinos de saída para filtros de multiplexador e filtros de autor de arquivo. Para obter mais informações, consulte [Renderizar um Project](rendering-a-project.md).

Para a versão prévia, você não precisa chamar esse método. Basta chamar **ConnectFrontEnd** seguido [**por IRenderEngine::RenderOutputPins.**](irenderengine-renderoutputpins.md)

Se o método retornar S \_ OK, a interface **IPin** retornada terá uma contagem de referência pendente. Certifique-se de liberar a interface quando terminar de usá-la.

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IRenderEngine Interface**](irenderengine.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




