---
description: O método ValidateSourceNames valida nomes de origem na linha do tempo, usando o localizador de mídia. Opcionalmente, esse método também atualiza qualquer objeto de origem para o qual ele localiza um arquivo.
ms.assetid: 8f4b9ff0-f283-4bcb-83f4-92410cead7db
title: 'Método IAMTimeline:: ValidateSourceNames (QEdit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.ValidateSourceNames
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5154926cb9f814c94762b556721c7580e5b0d82c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787143"
---
# <a name="iamtimelinevalidatesourcenames-method"></a>Método IAMTimeline:: ValidateSourceNames

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `ValidateSourceNames` método valida os nomes de origem na linha do tempo, usando o localizador de mídia. Opcionalmente, esse método também atualiza qualquer objeto de origem para o qual ele localiza um arquivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ValidateSourceNames(
   long          ValidateFlags,
   IMediaLocator *pOverride,
   long          NotifyEventHandle
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ValidateFlags* 
</dt> <dd>

Combinação de bits bit de [**sinalizadores de validação de nome de arquivo**](file-name-validation-flags.md) especificando o comportamento do localizador de mídia. Os \_ sinalizadores de verificação SFN VALIDATEF \_ replace e SFN \_ VALIDATEF \_ devem estar presentes ou o método retorna E \_ INVALIDARG.

</dd> <dt>

*pOverride* 
</dt> <dd>

Ponteiro opcional para a interface [**IMediaLocator**](imedialocator.md) de um localizador de mídia a ser usado no lugar do padrão. Para usar o localizador de mídia padrão, defina o valor desse parâmetro como **NULL**. Consulte comentários para obter mais informações.

</dd> <dt>

*NotifyEventHandle* 
</dt> <dd>

Identificador para um evento. O método sinaliza o evento depois de concluir a validação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Usando o parâmetro *pOverride* , você pode fornecer sua própria implementação personalizada da interface [**IMediaLocator**](imedialocator.md) . Por exemplo, o localizador de mídia padrão não notificará seu aplicativo sobre os arquivos que ele encontra (ou não pode localizar). Para contornar essa limitação, você pode implementar um localizador de mídia personalizado, tornando-o um wrapper para a versão padrão. Em sua versão personalizada, passe [**IMediaLocator:: FindMediaFile**](imedialocator-findmediafile.md) chamadas diretamente para a versão padrão e examine o valor de retorno.

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

[**Interface IAMTimeline**](iamtimeline.md)
</dt> <dt>

[Códigos de erro e êxito](error-and-success-codes.md)
</dt> </dl>

 

 




