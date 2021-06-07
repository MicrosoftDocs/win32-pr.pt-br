---
title: Propriedade IVMVirtualPC DefaultVMConfigurationPath (VPCCOMInterfaces. h)
description: Diretório padrão a ser procurado por arquivos de configuração de máquina virtual disponíveis.
ms.assetid: 9ae63198-e3f6-4dcb-8edb-85adfbbdca26
keywords:
- Propriedade DefaultVMConfigurationPath Virtual PC
- Propriedade DefaultVMConfigurationPath Virtual PC, interface IVMVirtualPC
- IVMVirtualPC interface virtual PC, Propriedade DefaultVMConfigurationPath
topic_type:
- apiref
api_name:
- IVMVirtualPC.DefaultVMConfigurationPath
- IVMVirtualPC.get_DefaultVMConfigurationPath
- IVMVirtualPC.put_DefaultVMConfigurationPath
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09f6370dfb868ec386e05f361240a74412f13a7d
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387632"
---
# <a name="ivmvirtualpcdefaultvmconfigurationpath-property"></a>IVMVirtualPC: Propriedade efaultVMConfigurationPath de:D

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera e define o diretório padrão a ser procurado por arquivos de configuração de máquina virtual disponíveis.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_DefaultVMConfigurationPath(
  [in]          BSTR configurationPath
);

HRESULT get_DefaultVMConfigurationPath(
  [out, retval] BSTR *configurationPath
);
```



## <a name="property-value"></a>Valor da propriedade

Especifica o caminho do diretório para os arquivos de configuração padrão da máquina virtual. Na cadeia de caracteres de caminho, uma barra invertida ( \\ ) pode aparecer imediatamente antes do caractere nulo de terminação.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                               | Significado                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                                  | A operação foi bem-sucedida.<br/>                                                                                                                 |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                                    | O parâmetro *configurationPath* é **nulo**.<br/>                                                                                                |
| <dl> <dt>HRESULT \_ Do \_ Win32 (arquivo de erro \_ \_ não \_ encontrado)</dt> <dt>0x80070002</dt> </dl> | O sistema não pode localizar o diretório especificado pelo parâmetro *configurationPath* .<br/>                                                          |
| <dl> <dt>HRESULT \_ Do \_ Win32 (caminho de erro \_ \_ não \_ encontrado)</dt> <dt>0x80070003</dt> </dl> | O sistema não pode localizar o caminho especificado pelo parâmetro *configurationPath* .<br/>                                                               |
| <dl> <dt>HRESULT \_ DO \_ Win32 ( \_ \_ nome inválido do erro)</dt> <dt>0x8007007b</dt> </dl>    | O parâmetro *configurationPath* contém um caractere inválido (um dos seguintes: " \* ? <>/ \| ": ").<br/>                                   |
| <dl> <dt>HRESULT \_ Do \_ Win32 ( \_ nome de \_ caminho inadequado de erro)</dt> <dt>0x800700a1</dt> </dl>    | O parâmetro *configurationPath* especifica um caminho relativo ou vazio. Um caminho absoluto é necessário.<br/>                                          |
| <dl> <dt>HRESULT \_ Do \_ Win32 (estouro de buffer de erro \_ \_ )</dt> <dt>0x8007006f</dt> </dl> | O caminho especificado pelo parâmetro *configurationPath* é muito longo. O comprimento do caminho deve ser menor que o **\_ caminho máximo** (260) caracteres.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>                            | Ocorreu um erro inesperado.<br/>                                                                                                             |
| <dl> <dt>VM \_ E 0xA0040951 de \_ \_ virtualização de hardware \_ desabilitada</dt> <dt></dt> </dl>     | O processador não oferece suporte a extensões de corre (virtualização acelerada por hardware).<br/>                                                          |



## <a name="remarks"></a>Comentários

Por padrão, esse valor de propriedade é definido como o seguinte diretório: "% LocalAppData% \\ Microsoft \\ Windows Virtual PC \\ Virtual Machines \\ ".

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualPC é definido como 236ba0d9-a24a-4292-a132-27c1421dfd01<br/>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMVirtualPC**](ivmvirtualpc.md)
</dt> </dl>

 

