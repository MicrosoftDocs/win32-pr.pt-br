---
title: Método IVMVirtualPC GetDVDFiles (VPCCOMInterfaces. h)
description: Recupera uma matriz de arquivos de DVD conhecidos.
ms.assetid: 9fe2191f-c5c0-464d-a190-29b2aba69682
keywords:
- GetDVDFiles do método virtual PC
- Método GetDVDFiles Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método GetDVDFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetDVDFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a91d7f0d65d1f62feb21d41bd9b27bf6ce112ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105763180"
---
# <a name="ivmvirtualpcgetdvdfiles-method"></a>Método IVMVirtualPC:: GetDVDFiles

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera uma matriz de arquivos de DVD conhecidos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetDVDFiles(
  [in]          VARIANT inAdditionalSearchPaths,
  [out, retval] VARIANT *outDVDFileList
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*inAdditionalSearchPaths* \[ no\]
</dt> <dd>

Esses caminhos serão pesquisados juntamente com os caminhos definidos na propriedade [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) .

</dd> <dt>

*outDVDFileList* \[ out, retval\]
</dt> <dd>

Uma matriz de arquivos de DVD virtuais encontrada nos caminhos de pesquisa especificados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                        | Descrição                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | A operação foi bem-sucedida.<br/>                                                        |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                                | O parâmetro *outDVDFileList* é **nulo**.<br/>                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                             | O parâmetro *inAdditionalSearchPaths* não é uma matriz de cadeias de caracteres.<br/>                  |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                        | Ocorreu um erro inesperado.<br/>                                                    |
| <dl> <dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt> </dl> | O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).<br/> |



 

## <a name="remarks"></a>Comentários

Os caminhos de pesquisa usados para recuperar a matriz de arquivos incluirão aqueles definidos anteriormente por [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) além daqueles especificados pelo parâmetro *inAdditionalSearchPaths* e o local do instalador para o módulo componentes de integração.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

