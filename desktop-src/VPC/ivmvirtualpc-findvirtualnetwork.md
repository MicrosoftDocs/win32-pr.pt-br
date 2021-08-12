---
title: Método IVMVirtualPC FindVirtualNetwork (VPCCOMInterfaces. h)
description: Recupera um objeto de rede virtual que corresponde ao nome solicitado.
ms.assetid: 84526fa4-fe88-4466-866d-c432ed3125aa
keywords:
- FindVirtualNetwork do método virtual PC
- Método FindVirtualNetwork Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método FindVirtualNetwork
topic_type:
- apiref
api_name:
- IVMVirtualPC.FindVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc8cfb0b8f9b7ee5be7bfb25d7d4cd7ca7b215bcf1824262c576038e75e6ce0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118592131"
---
# <a name="ivmvirtualpcfindvirtualnetwork-method"></a>Método IVMVirtualPC:: FindVirtualNetwork

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera um objeto de rede virtual que corresponde ao nome solicitado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT FindVirtualNetwork(
  [in]          BSTR              virtualNetworkName,
  [out, retval] IVMVirtualNetwork **virtualNetwork
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*virtualNetworkName* \[ no\]
</dt> <dd>

O nome da rede virtual a ser localizada.

</dd> <dt>

*virtualNetwork* \[ out, retval\]
</dt> <dd>

Um ponteiro para um novo objeto [**IVMVirtualNetwork**](ivmvirtualnetwork.md) que representa essa rede virtual.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                            | Descrição                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                                  | A operação foi bem-sucedida.<br/>                                                        |
| <dl> <dt>**S \_ FALSO**</dt> <dt>1</dt> </dl>                                               | Não foi possível encontrar a rede virtual especificada.<br/>                                    |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                                    | O parâmetro *virtualNetwork* é **nulo** ou a rede virtual não foi encontrada.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | O parâmetro *virtualNetworkName* não é válido ou é uma cadeia de caracteres vazia.<br/>               |
| <dl> <dt>**HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)**</dt> <dt>0x80070002</dt> </dl> | Não foi possível encontrar o arquivo de rede virtual.<br/>                                         |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                            | Ocorreu um erro inesperado.<br/>                                                    |
| <dl> <dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt> </dl>     | O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).<br/> |



 

## <a name="remarks"></a>Comentários

Os nomes de rede virtual não diferenciam maiúsculas de minúsculas, por exemplo, "mynetwork" e "mynetwork" referem-se à mesma rede virtual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

