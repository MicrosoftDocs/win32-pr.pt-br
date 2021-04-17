---
description: Para que um aplicativo seja executado corretamente, o computador host deve ter as DLLs apropriadas instaladas. Essas DLLs podem ser fornecidas pelo sistema operacional ou pelo pacote redistribuível dos aplicativos.
ms.assetid: fa5405e9-116f-4b7f-8f8e-791a79942570
title: Vinculando bibliotecas estáticas e dinâmicas (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a7050b8a3b5e1e2544883eb140b67d50bc3cd11
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813310"
---
# <a name="linking-static-and-dynamic-libraries-direct3d-10"></a>Vinculando bibliotecas estáticas e dinâmicas (Direct3D 10)

Para que um aplicativo seja executado corretamente, o computador host deve ter as DLLs apropriadas instaladas. Essas DLLs podem ser fornecidas pelo sistema operacional ou pelo pacote redistribuível dos aplicativos.

## <a name="libraries-load-appropriate-dlls"></a>Bibliotecas carregam DLLs apropriadas

As bibliotecas incluídas no SDK do DirectX carregarão automaticamente as DLLs apropriadas no tempo de execução. A exceção a essa regra é d3dx10. lib/d3dx10d. lib, que carregará o d3dx10.dll enviado com essa versão do SDK. Por exemplo, se o SDK baixado incluir d3dx10 \_33.dll e d3dx10 \_34.dll, a biblioteca (d3dx10. lib) que foi enviada com esse SDK carregará d3dx10 \_34.dll. Se um SDK subsequente for instalado mais tarde contendo d3dx10 \_ 35. lib, o d3dx10. lib do SDK anterior ainda carregará d3dx10 \_34.dll. O d3dx10. lib do SDK mais recente irá carregar o d3dx10 \_35.dll.

## <a name="redistributing-binaries"></a>Redistribuindo binários

Somente d3dx10.dll (e as versões subsequentes do mesmo arquivo) podem ser redistribuídas. Para redistribuir esse arquivo, você deve usar a função **DirectXSetup** . Para obter detalhes sobre como usar essa função e como reunir um pacote redistribuível, consulte [instalando o DirectX com DirectSetup](https://msdn.microsoft.com/library/Ee418267(v=VS.85).aspx). Todos os outros binários necessários estão incluídos no Windows Vista. Os únicos binários que podem ser redistribuídos são os localizados no diretório a seguir.


```
(SDK root)\Redist
```



A tabela a seguir descreve os binários dos quais os desenvolvedores devem estar cientes.



| Binários do Direct3D 10   | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| d3dx10.dll/d3dx10d.dll | Componentes de D3DX10 de varejo e depuração; os componentes de varejo podem ser redistribuídos no CAB Redist.                                                                                                                                                                                                                                                                                                                                                                                                             |
| d3d10ref.dll           | Rasterizador de referência. Fornece a implementação de software do pipeline de gráficos. Incluído apenas como parte do SDK do Windows ou SDK herdado do DirectX e não pode ser redistribuído. O rasterizador de referência destina-se somente à depuração. A vinculação explícita não é necessária; a tentativa de criar um dispositivo de referência (consulte [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice)) carregará essa dll, se ela estiver presente.                                                                                                    |
| d3d10sdklayers.dll     | Uma série de utilitários do SDK que atuam como uma camada entre chamadas de API e execução em tempo de execução, incluindo a [camada de depuração](d3d10-graphics-programming-guide-api-features-layers.md) e a camada de switch-to-Reference. A vinculação explícita não é necessária; se um dispositivo for criado com o sinalizador de camada apropriado, essa DLL será carregada automaticamente. Esse componente destina-se apenas a fins de desenvolvimento e depuração. Incluído apenas como parte do SDK do Windows ou SDK herdado do DirectX e não pode ser redistribuído. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> <dt>

[Gráficos do Direct3D 10](d3d10-graphics.md)
</dt> </dl>

 

 



