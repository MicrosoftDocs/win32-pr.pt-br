---
title: Método IVMVirtualPC GetVirtualMachineFiles (VPCCOMInterfaces. h)
description: Recupera uma matriz de arquivos de configuração de máquina virtual conhecidos.
ms.assetid: 38771573-66fa-408a-95db-1281efdf8b73
keywords:
- GetVirtualMachineFiles do método virtual PC
- Método GetVirtualMachineFiles Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, método GetVirtualMachineFiles
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetVirtualMachineFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ae2f96fb0c289f155158c77cdf3e4a8df1cb83aa8a51e0329d9fcd835ea4d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998596"
---
# <a name="ivmvirtualpcgetvirtualmachinefiles-method"></a>Método IVMVirtualPC:: GetVirtualMachineFiles

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera uma matriz de arquivos de configuração de máquina virtual conhecidos.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetVirtualMachineFiles(
  [in]          VARIANT      inAdditionalSearchPaths,
  [in]          VARIANT_BOOL inExcludedRegisteredVMs,
  [out, retval] VARIANT      *outVirtualMachineFileList
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*inAdditionalSearchPaths* \[ no\]
</dt> <dd>

Esses caminhos serão pesquisados juntamente com os caminhos definidos nas propriedades [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) e [**IVMVirtualPC::D efaultvmconfigurationpath**](ivmvirtualpc-defaultvmconfigurationpath.md) .

</dd> <dt>

*inExcludedRegisteredVMs* \[ no\]
</dt> <dd>

**True** se as máquinas virtuais registradas devem ser excluídas do retorno da matriz no parâmetro *outVirtualMachineFileList* ; caso contrário, **false** .

</dd> <dt>

*outVirtualMachineFileList* \[ out, retval\]
</dt> <dd>

Uma matriz de cadeias de caracteres de caminho para os arquivos de configuração de máquina virtual encontrados nos caminhos de pesquisa especificados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                                        | Descrição                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                              | A operação foi bem-sucedida.<br/>                                                        |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>                                | O parâmetro *outVirtualMachineFileList* é **nulo**.<br/>                               |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                             | O parâmetro *inAdditionalSearchPaths* não é uma matriz de cadeias de caracteres.<br/>                  |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>                        | Ocorreu um erro inesperado.<br/>                                                    |
| <dl> <dt>**VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada**</dt> <dt></dt> </dl> | O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).<br/> |



 

## <a name="remarks"></a>Comentários

Os caminhos de pesquisa usados para recuperar a matriz de arquivos de configuração incluirão aqueles definidos anteriormente por [**IVMVirtualPC:: SearchPaths**](ivmvirtualpc-searchpaths.md) e [**IVMVirtualPC::D efaultvmconfigurationpath**](ivmvirtualpc-defaultvmconfigurationpath.md) além daqueles especificados pelo parâmetro *inAdditionalSearchPaths* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

