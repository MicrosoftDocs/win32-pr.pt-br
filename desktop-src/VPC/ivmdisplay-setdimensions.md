---
title: Método IVMDisplay SetDimensions (VPCCOMInterfaces.h)
description: Define a altura e a largura da exibição da VM, em pixels.
ms.assetid: 8ad5cfc4-59b4-4327-b088-d54adf9c6fda
keywords:
- Computador Virtual do método SetDimensions
- Método SetDimensions Pc Virtual, interface IVMDisplay
- COMPUTADOR Virtual da interface IVMDisplay, método SetDimensions
topic_type:
- apiref
api_name:
- IVMDisplay.SetDimensions
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bbf1db342342e9fbb8c0eff2df18f9c2a76443a4d20014bad34934ccecd3dfb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119473356"
---
# <a name="ivmdisplaysetdimensions-method"></a>Método IVMDisplay::SetDimensions

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define a altura e a largura da exibição da máquina virtual (VMs) em pixels.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetDimensions(
  [in] long displayPixelWidth,
  [in] long displayPixelHeight
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*displayPixelWidth* \[ Em\]
</dt> <dd>

A largura, em pixels. O valor deve estar entre os valores de 640 e 2048. Se o valor não for divisível por 8, ele será reduzido para o próximo múltiplo inferior de 8.

</dd> <dt>

*displayPixelHeight* \[ Em\]
</dt> <dd>

A altura, em pixels. O valor deve estar entre os valores de 480 e 1920.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                                    | Descrição                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                          | A operação foi bem-sucedida.<br/>                                                                                                                                                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                         | O *parâmetro displayPixelWidth* não é divisível por 8 ou o *parâmetro displayPixelWidth* ou *displayPixelHeight* está fora dos valores mínimos permitidos (640x480) ou máximo de 2048x1920).<br/> |
| <dl> <dt>**VM \_ E \_ TIMED \_ OUT**</dt> <dt>0xA0040202</dt> </dl>                     | A alteração da resolução não foi finalizada em tempo hábil.<br/>                                                                                                                                              |
| <dl> <dt>**VM \_ E \_ VM \_ NÃO \_ EXECUTANDO**</dt> <dt>0XA0040206</dt> </dl>               | A máquina virtual deve estar em execução para essa operação.<br/>                                                                                                                                               |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>                    | A máquina virtual não é válida ou não está em execução no momento.<br/>                                                                                                                                         |
| <dl> <dt>**VM \_ E \_ NO \_ DISPLAY**</dt> <dt>0XA0040850</dt> </dl>                    | Não é possível localizar uma exibição válida para a VM.<br/>                                                                                                                                                          |
| <dl> <dt>**VM \_ O \_ RECURSO DE \_ ADIÇÕES E NÃO \_ \_ ESTÁ**</dt> <dt>0XA0040505</dt> </dl> | A versão dos componentes de integração instalados no sistema operacional convidado não dá suporte a essa operação.<br/>                                                                                    |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>                    | Ocorreu um erro inesperado.<br/>                                                                                                                                                                     |



 

## <a name="remarks"></a>Comentários

O tamanho mínimo da exibição da máquina virtual é de 640 x 480 pixels. O tamanho máximo é 2048 x 1920. As tentativas de definir o tamanho de exibição como valores fora desses limites ou para qualquer largura que não seja divisível por 8 resultarão no retorno de **um erro E \_ INVALIDARG.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMDisplay é definido como \_ 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

