---
description: Especifica se a complexidade do algoritmo de codificação de áudio está restrita.
ms.assetid: a50b840f-9fe8-4291-b93f-f09c241fe802
title: Propriedade MFPKEY_CONSTRAINENCOMPLEXITY (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc6e3d5a7077c72e5933ecbc235092174e263fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797554"
---
# <a name="mfpkey_constrainencomplexity-property"></a>\_Propriedade MFPKEY CONSTRAINENCOMPLEXITY

Especifica se a complexidade do algoritmo de codificação de áudio está restrita.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

Disponível apenas usando [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Tipo de Dados

**BOOL do VT \_**

## <a name="default-value"></a>Valor padrão

**VARIANTE \_ falso**

## <a name="remarks"></a>Comentários

Se você deixar essa propriedade com seu valor padrão de **variante \_ false**, o codificador de áudio usará seu algoritmo padrão. O algoritmo padrão depende do tipo de saída e da versão do Windows em execução. A tabela a seguir descreve o comportamento padrão para as diferentes combinações.



| Sistema operacional | Comportamento padrão                                                                                                                                                                                    |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista    | Para todos os tipos de saída, o codificador de áudio usa o algoritmo mais complexo por padrão.                                                                                                                 |
| Windows 7        | Para tipos de saída standard e Professional, o codificador de áudio usa o algoritmo mais complexo por padrão. Para tipos de saída sem perdas, o codificador de áudio usa o algoritmo menos complexo por padrão. |



 

Se você definir essa propriedade como **Variant \_ true**, também deverá especificar um valor de complexidade definindo a propriedade [**MFPKEY \_ ENCCOMPLEXITY**](mfpkey-enccomplexityproperty.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
