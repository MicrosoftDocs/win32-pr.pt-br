---
title: Método IVMKeyboard TypeKeySequence (VPCCOMInterfaces. h)
description: Simula uma lista delimitada por vírgulas de chaves que estão sendo digitadas.
ms.assetid: ba4d4e43-cb2e-49ae-940d-2e81286d3473
keywords:
- TypeKeySequence do método virtual PC
- Método TypeKeySequence Virtual PC, interface IVMKeyboard
- IVMKeyboard interface virtual PC, método TypeKeySequence
topic_type:
- apiref
api_name:
- IVMKeyboard.TypeKeySequence
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565d31d04a31f72ea25b3477fb91d53d252f6173eec8bc2f40133db38eeb1619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998856"
---
# <a name="ivmkeyboardtypekeysequence-method"></a>Método IVMKeyboard:: TypeKeySequence

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Simula uma lista delimitada por vírgulas de chaves que estão sendo digitadas.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT TypeKeySequence(
  [in] BSTR keySequence
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*KeySequence* \[ no\]
</dt> <dd>

A sequência delimitada por vírgulas de códigos de chave a serem digitados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                 | Descrição                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>                                   |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro é **NULL**.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>      | A cadeia de caracteres especificada está vazia ou contém um código de chave inválido.<br/> |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/>                               |



 

## <a name="remarks"></a>Comentários

Uma cadeia de caracteres de sequência de chave é um conjunto delimitado por vírgulas de identificadores de chave que são usados para simular o pressionamento de tecla e a sequência de versão de um teclado em estilo padrão dos EUA 101.

Se um identificador de chave aparecer na cadeia de caracteres sem um modificador anterior, um código com pressionamento de tecla será enviado para a sessão da máquina virtual, seguido imediatamente pelo código de lançamento de chave correspondente. Os modificadores de chave podem ser usados para alterar esse comportamento.

Por exemplo, o modificador DOWN enviará o código de chave pressionada para o identificador de chave a seguir sem enviar o código de lançamento de chave. Isso é útil para simular as teclas CTRL, ALT e Shift quando elas são mantidas enquanto outras chaves estão sendo enviadas. Para liberar a chave, ela deve ser incluída na cadeia de caracteres de chave novamente junto com um modificador UP anterior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard é definido como 00695f2e-c5ad-4d6e-B1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> <dt>

[Sequências de chave](key-sequences.md)
</dt> </dl>

 

