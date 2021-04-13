---
title: Método SendKeys IMsRdpClientNonScriptable
description: Envia uma série de pressionamentos de teclas para o controle. Os pressionamentos de tecla estão no formato de código de digitalização, que são os dados de teclado das chaves físicas reais.
ms.assetid: 1f07a9cc-4795-43cb-ac99-4bb70b8b544a
ms.tgt_platform: multiple
keywords:
- Método SendKeys Serviços de Área de Trabalho Remota
- Método SendKeys Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable, método SendKeys
- Método SendKeys Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable2
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable2, método SendKeys
- Método SendKeys Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable3
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable3, método SendKeys
- Método SendKeys Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable4
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable4, método SendKeys
- Método SendKeys Serviços de Área de Trabalho Remota, interface IMsRdpClientNonScriptable5
- Serviços de Área de Trabalho Remota de interface IMsRdpClientNonScriptable5, método SendKeys
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.SendKeys
- IMsRdpClientNonScriptable2.SendKeys
- IMsRdpClientNonScriptable3.SendKeys
- IMsRdpClientNonScriptable4.SendKeys
- IMsRdpClientNonScriptable5.SendKeys
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9effa3bbd40eb64df55914b9adbc07a03ea0c465
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455496"
---
# <a name="imsrdpclientnonscriptablesendkeys-method"></a>Método IMsRdpClientNonScriptable:: SendKeys

Envia uma série de pressionamentos de teclas para o controle. Os pressionamentos de tecla estão no formato de código de digitalização, que são os dados de teclado das chaves físicas reais.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SendKeys(
  [in] LONG         numKeys,
  [in] VARIANT_BOOL *pbArrayKeyUp,
  [in] LONG         *plKeyData
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*numKeys* \[ no\]
</dt> <dd>

O número de pressionamentos de teclas a serem enviados. O número máximo de chaves que podem ser enviadas em uma operação é 20. O método retornará **E \_ INVALIDARG** se esse parâmetro for maior que 20. Para obter mais informações, consulte a seção Comentários a seguir.

</dd> <dt>

*pbArrayKeyUp* \[ no\]
</dt> <dd>

Uma matriz cujo tamanho é igual a *numKeys*. Um elemento será **true** se a chave correspondente for up e **false** se a chave correspondente estiver inoperante.

</dd> <dt>

*plKeyData* \[ no\]
</dt> <dd>

Uma matriz cujo tamanho é igual a *numKeys*. A matriz contém dados de pressionamento de tecla e corresponde ao valor do parâmetro *lParam* da mensagem [ \_ KEYDOWN do WM](../inputdev/wm-keydown.md) . Os dados especificam a contagem de repetição, o código de verificação, o sinalizador de chave estendida, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição. Para obter uma descrição dos bits nessa matriz, consulte o [WM \_ KEYDOWN](../inputdev/wm-keydown.md).

O elemento correspondente em *pbArrayKeyUp* indica se a chave está para cima ou para baixo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornar **S \_ OK** se for bem-sucedido.

## <a name="remarks"></a>Comentários

O método **SendKeys** não mistura pressionamentos de teclas feitos pelo usuário local com pressionamentos de teclas que o método está enviando. Todos os pressionamentos de teclas passados para o método são enviados para a sessão remota em uma única sequência atômica.

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                     |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                               |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable é definido como 2f079c4c-87b2-4AFD-97ab-20cdb43038ae<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[o WM \_ KEYDOWN](../inputdev/wm-keydown.md)
</dt> </dl>

 

