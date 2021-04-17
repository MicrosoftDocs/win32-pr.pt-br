---
title: Método setdimensions IVMDisplay (VPCCOMInterfaces. h)
description: Define a altura e a largura da exibição da VM, em pixels.
ms.assetid: 8ad5cfc4-59b4-4327-b088-d54adf9c6fda
keywords:
- Método setdimensions Virtual PC
- Método setdimensions Virtual PC, interface IVMDisplay
- IVMDisplay interface virtual PC, método setdimensions
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
ms.openlocfilehash: 4730d73e06074714c8e6ed31fda992259d5c19ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759588"
---
# <a name="ivmdisplaysetdimensions-method"></a>Método IVMDisplay:: setdimensions

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define a altura e a largura da exibição da máquina virtual (VM), em pixels.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetDimensions(
  [in] long displayPixelWidth,
  [in] long displayPixelHeight
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*displayPixelWidth* \[ no\]
</dt> <dd>

A largura, em pixels. O valor deve estar entre os valores de 640 e 2048. Se o valor não for igualmente divisível por 8, ele será reduzido para o próximo múltiplo inferior de 8.

</dd> <dt>

*displayPixelHeight* \[ no\]
</dt> <dd>

A altura, em pixels. O valor deve estar entre os valores de 480 e 1920.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                    | Descrição                                                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                          | A operação foi bem-sucedida.<br/>                                                                                                                                                                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                         | O parâmetro *displayPixelWidth* não é divisível por 8, ou o parâmetro *displayPixelWidth* ou *displayPixelHeight* está fora dos valores mínimos permitidos (640x480) ou máximo de 2048x1920).<br/> |
| <dl> <dt>**VM \_ E \_ atingiu o tempo \_ limite**</dt> de <dt>0xA0040202</dt> </dl>                     | A alteração de resolução não foi concluída em tempo hábil.<br/>                                                                                                                                              |
| <dl> <dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt> </dl>               | A máquina virtual deve estar em execução para esta operação.<br/>                                                                                                                                               |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>                    | A máquina virtual não é válida ou não está em execução no momento.<br/>                                                                                                                                         |
| <dl> <dt>**VM \_ E \_ nenhum \_**</dt> <dt>0xA0040850</dt> de exibição </dl>                    | Não é possível localizar uma exibição válida para a VM.<br/>                                                                                                                                                          |
| <dl> <dt>**VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP**</dt> . <dt>0xA0040505</dt> </dl> | A versão dos componentes de integração instalados no sistema operacional convidado não oferece suporte a essa operação.<br/>                                                                                    |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                    | Ocorreu um erro inesperado.<br/>                                                                                                                                                                     |



 

## <a name="remarks"></a>Comentários

O tamanho mínimo da exibição da máquina virtual é de 640 x 480 pixels. O tamanho máximo é 2048 x 1920. As tentativas de definir o tamanho de exibição para valores fora desses limites, ou para qualquer largura que não seja divisível por 8, resultarão no retorno de um erro **E \_ INVALIDARG** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay é definido como 960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

