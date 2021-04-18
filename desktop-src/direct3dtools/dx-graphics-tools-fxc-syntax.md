---
title: Sintaxe
description: Aqui está a sintaxe para chamar FXC.exe, a ferramenta de compilador de efeito. Para obter um exemplo, consulte compilando offline.
ms.assetid: 3aee89bd-02e1-4de1-8552-ba36814f8464
keywords:
- FXC, sintaxe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6241a728b4835b11d10ea6e39d67fd73a8576cd7
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "105781560"
---
# <a name="syntax"></a>Sintaxe

Aqui está a sintaxe para chamar FXC.exe, a ferramenta de compilador de efeito. Para obter um exemplo, consulte [compilando offline](dx-graphics-tools-fxc-using.md).

-   [Usage](#usage)
-   [Argumentos](#arguments)
-   [Comentários](#remarks)
-   [Perfis](#profiles)
-   [Notas de versão](#version-notes)
-   [Tópicos relacionados](#related-topics)

## <a name="usage"></a>Uso

*nomes* de **FXC** do *switchoptions*

## <a name="arguments"></a>Argumentos
Separe cada opção de comutador com um espaço ou dois-pontos.

### <a name="switchoptions"></a>*Switchoptions*
\[em \] Opções de compilação. Há apenas uma opção necessária e muito mais que são opcionais. Separe cada um com um ou dois espaços.

#### <a name="required-option"></a>Opção necessária
##### <a name="t-profile"></a>/T <*perfil*>
Modelo de sombreador (consulte [perfis](#profiles)).

#### <a name="optional-options"></a>Opções opcionais
##### <a name="-help"></a>/?, /help
Imprimir ajuda para `FXC.exe` .

##### <a name="commandoptionfile"></a>@<*comando. Option. File*>
Arquivo que contém opções de compilação adicionais. Essa opção pode ser combinada com outras opções de compilação de linha de comando. O *comando. Option. File* deve conter apenas uma opção por linha. O *comando. Option. File* não pode conter nenhuma linha em branco. As opções especificadas no arquivo não devem conter espaços à esquerda ou à direita.

##### <a name="all_resources_bound"></a>/all_resources_bound
Habilite o nivelamento agressivo no SM 5.1 +. Novo para o Direct3D 12.

##### <a name="cc"></a>/CC
Assembly com código de cor de saída.

##### <a name="compress"></a>/compress
Compacte o código de bytes do sombreador DX10 dos arquivos.

##### <a name="d-idtext"></a>/D < >=< *texto* da ID>
Definir macro.

##### <a name="decompress"></a>/decompress
Descompacte o código de bytes do sombreador DX10 do primeiro arquivo. Os arquivos de saída devem ser listados na ordem em que estavam durante a compactação.

##### <a name="dumpbin"></a>/dumpbin
Carrega um arquivo binário em vez de compilar um sombreador.

##### <a name="e-name"></a>/E <name>
Ponto de entrada do sombreador. Se nenhum ponto de entrada for fornecido, **Main** será considerado o nome da entrada do sombreador.

##### <a name="enable_unbounded_descriptor_tables"></a>/enable_unbounded_descriptor_tables
Habilita tabelas de descritor não associadas. Novo para o Direct3D 12.

##### <a name="extractrootsignature-file"></a>*arquivo* de </extractrootsignature>
Extraia a assinatura raiz do código de bytes do sombreador. Novo para o Direct3D 12.

##### <a name="fc-file"></a>*Arquivo* de </FC>
Arquivo de listagem de código de assembly de saída.

##### <a name="fd-file"></a>*Arquivo* de </FD>
Extraia informações de PDB (banco de dados do programa do sombreador) e grave no arquivo fornecido. Ao compilar o sombreador, use/FD para gerar um arquivo PDB com informações de depuração do sombreador.

##### <a name="fe-file"></a>*Arquivo* de </FE>
Avisos de saída e erros para o arquivo fornecido.

##### <a name="fh-file"></a>*Arquivo* de </FH>
Arquivo de cabeçalho de saída que contém o código do objeto.

##### <a name="fl-file"></a>*Arquivo* de </FL
Saída de uma biblioteca. Requer o \_47.dll D3dcompiler ou uma versão posterior da dll.

##### <a name="fo-file"></a>/Fo <*arquivo*>
Arquivo de objeto de saída. Geralmente, dada a extensão &quot; . fxc &quot; , embora outras extensões sejam usadas, como &quot; . o &quot; , &quot; . obj &quot; ou &quot; . dxbc &quot; .

##### <a name="fx-file"></a>*Arquivo* de </FX>
Código do assembly de saída e arquivo de listagem Hex.

##### <a name="gch"></a>/Gch
Compile como um efeito filho para perfis de fx_4_x.

> [!NOTE]
> O suporte para perfis de efeitos herdados foi preterido.

##### <a name="gdp"></a>/Gdp
Desabilitar o modo de desempenho de efeito.

##### <a name="gec"></a>/Gec
Habilitar o modo de compatibilidade com versões anteriores.

##### <a name="ges"></a>/Ges
Habilite o modo estrito.

##### <a name="getprivate-file"></a>*arquivo* de </GetPrivate>
Salve dados privados do blob de sombreador (binário de sombreador compilado) no arquivo fornecido. Extrai dados privados, anteriormente inseridos por/SetPrivate, do blob de sombreador.

Você deve especificar a opção/DUMPBIN com/GetPrivate. Por exemplo:

```console
fxc /getprivate ps01.private.data 
    /dumpbin ps01.with.private.obj
```
    
##### <a name="gfa"></a>/Gfa
Evite construções de controle de fluxo.

##### <a name="gfp"></a>/GFP,
Prefira construções de controle de fluxo.

##### <a name="gis"></a>/Gis
Forçar restrição de IEEE.

##### <a name="gpp"></a>/Gpp
Forçar a precisão parcial.
    
##### <a name="i-include"></a>/I <*incluir*>
Caminho de inclusão adicional.

##### <a name="lx"></a>/Lx
Literais hexadecimais de saída. Requer o \_47.dll D3dcompiler ou uma versão posterior da dll.

##### <a name="matchuavs"></a>/matchUAVs
Corresponder as alocações do slot do UAV do sombreador de modelo no sombreador atual. Para obter mais informações, consulte <a href="#remarks">comentários</a>.

##### <a name="mergeuavs"></a>/mergeUAVs
Mescle as alocações do slot UAV do sombreador de modelo e o sombreador atual. Para obter mais informações, consulte <a href=""></a> <a href="#remarks">comentários</a>.

##### <a name="ni"></a>/Ni
Números de instrução de saída em listagens de assembly.

##### <a name="no"></a>/
Deslocamento de byte de instrução de saída em listagens de assembly. Quando você produzir o assembly, use////para anotar com o deslocamento de bytes para cada instrução.

##### <a name="nologo"></a>/nologo
Suprime uma mensagem de direitos autorais.

##### <a name="od"></a>/Od
Desabilitar otimizações. /OD implica/GFP,, mas a saída pode não ser idêntica a/OD/GFP.

##### <a name="op"></a>/Op
Desabilitar preshaders (preterido).

##### <a name="o0-o1-o2-o3"></a>/O0/O1,/O2,/O3
Níveis de otimização. O1 é a configuração padrão.
- O0-desabilita a reordenação de instrução. Isso ajuda a reduzir a carga de registro e permite uma simulação de loop mais rápida.
- O1-desabilita a reordenação de instrução para ps_3_0 e para cima.
- O2-igual a O1. Reservado para uso futuro.
- O3-igual a O1. Reservado para uso futuro.

##### <a name="p-file"></a>/P <*arquivo*>
Pré-processar para o arquivo (deve ser usado sozinho).

##### <a name="qstrip_debug"></a>/Qstrip_debug
Remova os dados de depuração do código de bytes do sombreador para 4_0 + perfis.

##### <a name="qstrip_priv"></a>/Qstrip_priv
Remova os dados privados do código de bytes 4_0 + Shader. Remove dados privados (sequência arbitrária de bytes) do blob de sombreador (binário de sombreador compilado) que você inseriu anteriormente com a `/setprivate <file>` opção.

Você deve especificar a opção/DUMPBIN com/Qstrip_priv. Por exemplo:

```console
fxc /Qstrip_priv /dumpbin /Fo ps01.no.private.obj 
    ps01.with.private.obj
```

##### <a name="qstrip_reflect"></a>/Qstrip_reflect
Remova os dados de reflexo do código de bytes do sombreador para 4_0 + perfis.

##### <a name="qstrip_rootsignature"></a>/Qstrip_rootsignature
Remova a assinatura raiz do código de bytes do sombreador. Novo para o Direct3D 12.

##### <a name="res_may_alias"></a>/res_may_alias
Suponha que UAVs/SRVs possa alias para cs_5_0 +. Requer o \_47.dll D3dcompiler ou uma versão posterior da dll.

##### <a name="setprivate-file"></a>*arquivo* de </SetPrivate>
Adicione dados privados no arquivo fornecido ao blob de sombreador compilado. Insere o arquivo fornecido, que é tratado como um buffer bruto, para o blob de sombreador. Use/SetPrivate para adicionar dados privados ao compilar um sombreador. Ou use a opção/DUMPBIN com/SetPrivate para carregar um objeto de sombreador existente e, depois que o objeto estiver na memória, para adicionar o blob de dados privados. Por exemplo, use um único comando com/SetPrivate para adicionar dados privados a um blob de sombreador compilado:

```console
fxc /T ps_4_0 /Fo ps01.with.private.obj ps01.fx 
    /setprivate ps01.private.data
```
    
Ou use dois comandos em que o segundo comando carrega um objeto de sombreador e, em seguida, adiciona dados privados:

```console
fxc /T ps_4_0 /Fo ps01.no.private.obj ps01.fx
fxc /dumpbin /Fo ps01.with.private.obj ps01.no.private.obj 
    /setprivate ps01.private.data
```
    
##### <a name="setrootsignature-file"></a>*arquivo* de </setrootsignature>
Anexe a assinatura raiz ao código de bytes do sombreador. Novo para o Direct3D 12.

##### <a name="shtemplate-file"></a>*arquivo* de </shtemplate>
Use o arquivo de sombreador de modelo fornecido para recursos de mesclagem (/mergeUAVs) e correspondentes (/matchUAVs). Para obter mais informações, consulte <a href="#remarks">comentários</a>.

##### <a name="vd"></a>/Vd
Desabilitar validação.

##### <a name="verifyrootsignature-file"></a>*arquivo* de </verifyrootsignature>
Verifique o código de bytes do sombreador em relação à assinatura raiz. Novo para o Direct3D 12.

##### <a name="vi"></a>/Vi
Exibir detalhes sobre o processo de inclusão.

##### <a name="vn-name"></a>*Nome* </vn>
Use nome como nome da variável no arquivo de cabeçalho.

##### <a name="wx"></a>/WX
Tratar avisos como erros.

##### <a name="zi"></a>/Zi
Habilitar informações de depuração.

##### <a name="zpc"></a>/Zpc
Matrizes de pacote na ordem de coluna principal.

##### <a name="zpr"></a>/Zpr
Matrizes de pacote na ordem de linha principal.

### <a name="filenames"></a>*Nomes de arquivos*

\[nos \] arquivos que contêm o (s) sombreador (es) e/ou os efeitos.

## <a name="remarks"></a>Comentários

Use as `/mergeUAVs` `/matchUAVs` Opções, e `/shtemplate` para alinhar os slots de associação UAV para uma cadeia de sombreadores.

Suponha que você tenha sombreadores A. FX, B. FX e C. FX. Para alinhar os slots de associação de UAV para essa cadeia de sombreadores, você precisa de duas passagens de compilação:

**Para alinhar os slots de associação de UAV para uma cadeia de sombreadores**

1.  Use/mergeUAVs para compilar sombreadores e especifique um blob de sombreador compilado anteriormente com/shtemplate. Por exemplo:
    ```
    fxc.exe /T cs_5_0 C.fx /Fo C.o /mergeUAVs /shtemplate Btmp.o
    ```
2.  Use/matchUAVs para compilar sombreadores e especifique o último blob de sombreador da primeira passagem com/shtemplate. Você pode compilar em qualquer ordem. Por exemplo:
    ```
    fxc.exe /T cs_5_0 A.fx /Fo A.o /matchUAVs /shtemplate C.o
    ```
Você não precisa recompilar o C. FX na segunda passagem.

Depois de executar as duas etapas de compilação anteriores, você pode usar um. o, B. o e o C. o como BLOBs de sombreador final com slots UAV alinhados.

## <a name="profiles"></a>Perfis

Cada modelo de sombreador é rotulado com um perfil HLSL. Para compilar um sombreador em um modelo de sombreador específico, escolha o perfil de sombreador apropriado na tabela a seguir.

<table><thead><tr class="header"><th>Tipo de Sombreador</th><th>Perfis</th></tr></thead><tbody><tr class="odd"><td>Sombreador de computação</td><td><dl> cs_4_0<br />
cs_4_1<br />
cs_5_0<br />
cs_5_1<br />
</dl></td></tr><tr class="even"><td>Sombreador de domínio</td><td><dl> ds_5_0<br />
ds_5_1<br />
</dl></td></tr><tr class="odd"><td>Sombreador de geometria</td><td><dl> gs_4_0<br />
gs_4_1<br />
gs_5_0<br />
gs_5_1<br />
</dl></td></tr><tr class="even"><td>Vinculação de sombreador HLSL </td><td><dl> lib_4_0<br />
lib_4_1<br />
lib_4_0_level_9_1<br />
lib_4_0_level_9_1_vs_only<br />
lib_4_0_level_9_1_ps_only<br />
lib_4_0_level_9_3<br />
lib_4_0_level_9_3_vs_only<br />
lib_4_0_level_9_3_ps_only<br />
lib_5_0<br />
</dl> Para obter mais informações sobre a vinculação de sombreador, consulte <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker"><strong>ID3D11Linker</strong></a> e <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph"><strong>ID3D11FunctionLinkingGraph</strong></a>. <br/></td></tr><tr class="odd"><td>{1&gt;Sombreador Hull&lt;1}</td><td><dl> hs_5_0<br />
hs_5_1<br />
</dl></td></tr><tr class="even"><td>Sombreador de pixel</td><td><dl> ps_2_0<br />
ps_2_a<br />
ps_2_b<br />
ps_2_sw<br />
ps_3_0<br />
ps_3_sw<br />
ps_4_0<br />
ps_4_0_level_9_0<br />
ps_4_0_level_9_1<br />
ps_4_0_level_9_3<br />
ps_4_1<br />
ps_5_0<br />
ps_5_1<br />
</dl></td></tr><tr class="odd"><td>Assinatura de raiz</td><td><dl> rootsig_1_0<br />
</dl></td></tr><tr class="even"><td>Sombreador de textura</td><td><dl> tx_1_0<br />
</dl></td></tr><tr class="odd"><td>Sombreador de vértice</td><td><dl> vs_1_1<br />
vs_2_0<br />
vs_2_a<br />
vs_2_sw<br />
vs_3_0<br />
vs_3_sw<br />
vs_4_0<br />
vs_4_0_level_9_0<br />
vs_4_0_level_9_1<br />
vs_4_0_level_9_3<br />
vs_4_1<br />
vs_5_0<br />
vs_5_1<br />
</dl></td></tr></tbody></table>

## <a name="version-notes"></a>Notas de versão

Para o Direct3D 12, consulte [especificando assinaturas raiz no HLSL](/windows/desktop/direct3d12/specifying-root-signatures-in-hlsl), [Associação de recursos em HLSL](/windows/desktop/direct3d12/resource-binding-in-hlsl) e [indexação dinâmica usando HLSL 5,1](/windows/desktop/direct3d12/dynamic-indexing-using-hlsl-5-1).

No Direct3D 10, use a API para obter o vértice, a geometria e o perfil do pixel-shader mais adequado para um determinado dispositivo chamando essas funções: [**D3D10GetVertexShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getvertexshaderprofile), [**D3D10GetPixelShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getpixelshaderprofile)e [**D3D10GetGeometryShaderProfile**](/windows/desktop/api/d3d10shader/nf-d3d10shader-d3d10getgeometryshaderprofile).

No Direct3D 9, use os métodos [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9-getdevicecaps) ou [**GetDeviceCaps**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getdevicecaps) para recuperar os perfis de vértice e pixel shader com suporte de um dispositivo. A estrutura [**D3DCAPS9**](/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9) retornada por esses métodos indica os perfis de vértice e pixel shader com suporte de um dispositivo em seus membros **VertexShaderVersion** e **PixelShaderVersion** .

Para obter exemplos, consulte [compilando com o compilador atual](dx-graphics-tools-fxc-using.md).

## <a name="related-topics"></a>Tópicos relacionados

* [Efeito-ferramenta do compilador](fxc.md)